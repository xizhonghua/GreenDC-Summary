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

### Current Solution
- Fair allocation
 - Drawback
  - do not offer the best performance and the above heuristics are compativle with a large class of fairness policies; 

### Proposed Solution
- The proposed solution Tetris adapts heuristics for the multidimensional bin packing problem to the context of cluster schedulers.
- Tetris imporve average job completion time by preferentially serving jobs that have less remaining work. 
- Tetris are compatible with a large class of fairness policies. Hence, we show how to simultaneously achieve good performance and fairness.

### Strongess


### Drawback

### Possible extension
