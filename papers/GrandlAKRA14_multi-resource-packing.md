## [Multi-Resource Packing for Cluster Schedulers](http://dl.acm.org/citation.cfm?id=2626334)

- started on 12/20/2014, end on
- bib
```
@inproceedings{Grandl:2014:MPC:2619239.2626334,
 author = {Grandl, Robert and Ananthanarayanan, Ganesh and Kandula, Srikanth and Rao, Sriram and Akella, Aditya},
 title = {Multi-resource Packing for Cluster Schedulers},
 booktitle = {Proceedings of the 2014 ACM Conference on SIGCOMM},
 year = {2014},
 pages = {455--466},
 numpages = {12}
} 
```

### Problem Statement
- Tasks in modern data-parallel clusters have high diverse resoruce requirements along CPU, memor, disk and network. 
- Thus, a multi-resource cluster scheduler is needed, which will be responsible for packing tasks to machines based on their requirements of all resource types. With the following objective
 - avoids resource fragmentation
 - avoid over-allocation of the resources that are not explicitly allocated

### Problem Model
- Task arrivals and machine availability change in an online manner and wherein task's resource needs change with time and with the machine that the task is placed at.
- Similar to bin-ball packing problem, however, 
 - balls are not know apriori, they arrive in online manner
 - need to consider the dependencies of tasks
 

### Current Solution
- Current schedulers neither pack tasks nor consider all their relevant resource demands. This results in fragmentation and over-allocation of resources, respectively.
 - Schedulers divide resurces into slots and offer the slots greeidly to the job that is furthest from its **fair share**. Such scheduling results in resource gragmentation, and the magnitude of which increase with the number of resource being allocated.
 - schedulers also **ignore disk and network requirments** of tasks. When assigning tasks to machines, they only check that tasks' CPU and memory needs are satisfiable. Hence, they can schedule many network or disk-intensive tasks o n the same machine. Such over-allocation leads to interference-disk seeks or network incase- that can sharply lower throughput. 
 - Through analysis, the authors show that the state-of-the-art schedulers in Facebook and Bing's analytics clusters delay job completions and increase makespan by 45%.
 
### Proposed Solution
- The proposed solution Tetris adapts heuristics for the multidimensional bin packing problem to the context of cluster schedulers.
 - Tetris imporve average job completion time by preferentially serving jobs that have less remaining work. 
 - Tetris are compatible with a large class of fairness policies. Hence, we show how to simultaneously achieve good performance and fairness.
- The underlying heuristic
 - learn task requirement t<sub>r</sub>, and monitor available resources at machines m<sub>r</sub>.
 - the packing heuristic projects t<sub>r</sub> and m<sub>r</sub> into enclidean space and picks the <task, machine> pair with the highest dot product value.
 - the dot product perfers large tasks and those that use resouces in proportions similar to what is available (prevents resource fragmentation)


### Strongess


### Drawback

### Possible extension
