## Task-aware Scheduling


### Motivation
Many data center applications perform rich and complex tasks (e.g., executing a search query or generating a user's news-feed). From a network perspective, these tasks typically comprise multiple flows, which traverse different parts of the network at potentially different times. [[Dogar-2014]](../papers/DogarK14_SIGCOMM_Decentralized-TaskScheduling-for-DCN.md)
- **Current**: Most network task resource allocation schemes, however, treat all these flows in isolation -- rather than as part of a task, and thereofore, only optimize flow-level metrics.
- **Future**: This has motivated efforts to allocate data center resources in a "task-aware" fashion. Examples include task-aware allocation of caches[[Ananthanarayanan-2012]](https://www.usenix.org/conference/nsdi12/technical-sessions/presentation/ananthanarayanan), network bandwidth [[Chowdhury-2011]](http://dl.acm.org/citation.cfm?id=2018448), and CPUs and network [[Ananthanarayanan-2010]](https://www.usenix.org/conference/osdi10/reining-outliers-map-reduce-clusters-using-mantri).
