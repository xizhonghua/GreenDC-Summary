## [Decentralized Task-aware Scheduling for Data Center Networks](http://research.microsoft.com/apps/pubs/default.aspx?id=215429)

- reading status: started on 12/17/2014
- bib
```
@Inproceedings {export:215429,
    author       = {Fahad R Dogar and Thomas Karagiannis and Hitesh Ballani and Ant Rowstron},
    booktitle    = {SIGCOMM},
    publisher    = {ACM},
    title        = {Decentralized Task-aware Scheduling for Data Center Networks},
    year         = {2014}
}
```

### Summary
In this paper, the author design decentralized task-aware scheduling approach that could reduce both the **average** as well as **tail completion time** for typical data center applications.
- The detail summary is [here](../file/task-aware.md)

### Comments
- It seems to me that the mechanism of task-aware scheduling  is studied in related works pFabric. But related work such as pFabric didn't consider heavy task workload which may hurt the performance of the completition time. Thus this paper proposed a mechanism to deal with this problem.
    - In particular, multiplexing is a mechanism to balance fairness and performance. For example, Hadoop fair scheduler allows limited multiplexing, although the limit is set by the user/administrator. However, the above mechanism is focusing on job scheduling, not on flow (or task) scheduling over the network and not on decentralized scheduling of flows, which requires new mechanism, as one descripbed in this paper.
    - The way of achieving multiplexing is to allow the task which is right after the heavy task to fair-share the resource together.
