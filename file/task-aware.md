## Task-aware Scheduling

- [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md)

### Definition
- Task-aware workloads: [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md) defines a task as the unit of work for an application that can be linked to a waiting user. 
  - Completition time: It is an important matric as it directly impacts user satisfication. 
  
|Fig: Common workflows in data center|
|:----|
|![](../fig/dc-flow.PNG)|


- Task characterization
  - the task size: tasks size distribution could be different depending on applications. For some applications, all tasks can be of similar size while others many have a heavy tailed distribution. [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md)
    - Hence, a general task-aware scheduling policy needs to be amenable to a wide-range of task size distributions, ranging from uniform to heavy-tailed.
  - the number of flows per task: flows per task can range from a few tens to hundreds, and as discussed earlier, subsets of flows can be active at different times and across different parts of the network.

### Motivation
Many data center applications perform rich and complex tasks (e.g., executing a search query or generating a user's news-feed). From a network perspective, these tasks typically comprise multiple flows, which traverse different parts of the network at potentially different times. [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md)
- **Current (flow-based resource allocation)**: Most network task resource allocation schemes, however, treat all these flows in isolation -- rather than as part of a task, and thereofore, only optimize flow-level metrics.
  - [[PDQ-2012]](http://dl.acm.org/citation.cfm?id=2342389), [[pFabric-2013]](http://dl.acm.org/citation.cfm?id=2486031): they can support a scheduling policy like shortest flow first (SFF), which minimize flow completion times by assigning resoruces based on flow size.
- **Future (task-based resource allocation)**: This has motivated efforts to allocate data center resources in a "task-aware" fashion. Examples include task-aware allocation of caches[[Ananthanarayanan-2012]](https://www.usenix.org/conference/nsdi12/technical-sessions/presentation/ananthanarayanan), network bandwidth [[Chowdhury-2011]](http://dl.acm.org/citation.cfm?id=2018448), and CPUs and network [[Ananthanarayanan-2010]](https://www.usenix.org/conference/osdi10/reining-outliers-map-reduce-clusters-using-mantri).


### Existing Approach
- Task serialization: We consider serving tasks one at a time. This can help finish tasks faster by reducing the amount of contention in the network. We define task serialization as the set of policies where an entire task is scheduled before moving to the next.
  - Question: can task-serialization also improve the tail task completition time?
- Task serialization policy
  - **FIFO**: Allocating network bandwidth to tasks in a FIFO fashion, such that they are scheduled over the network one at a time, can improve the average task completion time as compare to per-flow fair sharing (e.g., TCP) [[Chowdhury-2011]](http://dl.acm.org/citation.cfm?id=2018448)
    - Pros: 
      - simple
      - limits the maximum time a task has to wait, as a task's waiting time depends only on the task that arrive before it
      - It is proved to be optimal for minimizing the tail completion time, if task sizes follow a light tailed distribution, i.e., task sizes are faily homogeneous and do not follow a heavy tailed distribution [[Wierman-2012]](http://dl.acm.org/citation.cfm?id=2432678).
    - Cons: Since typical data center workloads include some fraction of heavy taskss (in terms of their network footprint), so obvious scheduling candidates like FIFO and size-based ordering perform poorly. For such applications, we need a policy that can seperate out these "elephants" from the small tasks. [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md)
  - **STF**:  schdules tasks based on their size. 
    - Pros: can guarantee good average performance.
    - Cons: can lead to high tail latency, or even starvation, for large sized tasks. Moreover, it requires knowledge about task sizs up front, which is impractical for many applications. 
  - **FIFO-LM**: (FIFO with limited multiplexing), a policy that schedules tasks based on their arrival order, but dynamically changes the level of multiplexing when heavy tasks are encountered. This ensures small tasks are not blocked behind heavy tasks that are, in turn, not starved [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md).
    - Pros: 
      - FIFO-LM (and even FIFO) can reduce both the average and the tail task completition times. 
      - They do so by smoothing bursty arrivals and ensuring that a tasks' completion is only impacted by tasks that arrive before it. For example, data center applications typically have multiple stages where a subsequent stage can only start when the previous stage finishes. In such scenarios, FIFO scheudling can smooth out a burst of tasks that arrive at the first stage. As a result, task observe less contention at the later stages, thereby smoothing the tail completion time. 
 
### BARRAT (FIFO-LM detail)
- How to determine a task is heavy
  - We assume that the data center has knowledge about task size distribution based on historically collected data. Based on this history, we need to identify a **threshold** (in terms of task size) beyong which we characterize a task as heavy. e.g., through the CDF curve in Figure 2 in [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md).
- How BARRAT is decentralized?
  - Each task is assigned a globally unique identifier (task-id) based on its arrival (or start) time.
  - Thus, switches can make decision without any coordination. Each switch makes the same decision based on the task priorityl.
  - Finally, switches locally decide when to increase the level of multiplexing through on-the-fly identification of heavy tasks. 
- How to assign the unique id to task?
  - We only need a single counter when all incoming tasks arrive through a common point. Examples of such common points include the load balancer (for user-facing applications like web search), the job scheduler (for data parallel and HPC applications), the meta-data manager (for storage applications), and so on.
  - We can use multiple counter when tasks arrive through multiple load balancers. Each counter has a unique start value and an incremental value. For example, if there are two counters, one of them generate odd task-ids (1,3,5,...), and one generate even task-ids (2, 4, 6, ...).
  - Note that the generation of task identifier should also account for background services (e.g., index update) that are part of most production data centers. But these tasks are assigned with strictly lower priority.
  - Propagation of task identifiers: all physical servers involve in a task need to know its task-id. Applications can propagate this identifier along the task workflow.
- Allow work-conservation and preemption
  - work-conservation: a lower priority task can be scheduled if the highest priority task is too small to saturate the lnk or if it is bottlenecked at a subsequent link.
  - premption: it is a complement of work-conservation. It ensures that the high priority task can grab back resources that assign to the high priority jobs.
  
### Simulation
- How to generate task-aware workloads?
  - [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md), each task has a global priority -- all flow within the task use this priority, irrespective of when these flow start and which part of the network they traverse. 
- How to generate heavy-tail workloads?
  - using Pareto or Lognormal distribution with varying parameters (shape or mean respectively)
- Evaluation metric
  - average and the tail (95th percentile and beyond) completition time.
  
### TO-CHECK
- What's the overhead?
- How to make sure of the global priority?
