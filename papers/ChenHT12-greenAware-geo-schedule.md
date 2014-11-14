## [Green-aware workload scheduling in geographically distributed data centers](http://dl.acm.org/citation.cfm?id=2469301)

- reading status: start 11/13/2014
- bib
```
@inproceedings{TangCH12,
 author = {Tang, Xueyan and Chen, Changbing and He, Bingsheng},
 title = {Green-aware Workload Scheduling in Geographically Distributed Data Centers},
 booktitle = {Proceedings of the 2012 IEEE 4th International Conference on Cloud Computing Technology and Science (CloudCom)},
 year = {2012},
 pages = {82--89},
 numpages = {8}
} 
```

### Summary
In this paper, the authors study the problem of minimizing brown energy consumption in distributed green data centers. 


### Model
- Job
 - A workload consists of many jobs, each of which is represented as a directed acyclic graph (DAG). Each node is a DAG represents a task. The job structure allows us to have finer grained scheduling on tasks.
 - Has deadline: each job has user specified QoS: each job has a specified deadline to define its slack.
- Objective
 - minimize power consumption
 
