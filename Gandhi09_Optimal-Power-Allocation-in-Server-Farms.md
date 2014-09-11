Optimal Power Allocation in Server Farms
---

- [PaperLink](http://www3.cs.stonybrook.edu/~anshul/sigmetrics_2009_tech.pdf)
- bib
```
@article{GaH09,
 author = {Gandhi, Anshul and Harchol-Balter, Mor and Das, Rajarshi and Lefurgy, Charles},
 title = {Optimal Power Allocation in Server Farms},
 journal = {SIGMETRICS Perform. Eval. Rev.},
 volume = {37},
 number = {1},
 month = jun,
 year = {2009},
 pages = {157--168},
 numpages = {12},
} 
```

### Background
- Server farms usually have a fixed peak power budget, since they are often billed by power suppliers based on their peak power requirement. The peak power budget of a server farm determines its cooling and power delivery infrastructure costs. Hence, companies are interested in maximizing the performance at a server farm given a fixed power budget.
- Power-to-frequency relationship.

### Summary
This paper investigates how to distributed available power among servers in a server farm so as to minimize mean response time, i.e., maximize performance.
- First, they investigated how power allocation affects server frequency in a single server using, DFS, DVFS, and DVFS+DFS for various workloads.
- Then they develop a queueing theoretical model which predicts the mean response time for a server farm as a function of many factors including the power-to-frequency relationship, arrival rate, peak power budget etc. The queuing model allow they to determine the optimal power allocation for every possible configuration of the above factors. 

### Model
1. Job arrival satisfy Poisson distribution.
2. Servers are constrainted by peak power budget. The CPU frequecy, voltage of each machine can be tuned in order under the constraints with objective to minmize mean resonse time.

### Strongness
1. They captured the power-to-frequency relationship under DFS and DFVS by experiments on CPU bound LINPACK workload.
2. The main idea is to decide the power allocation based on the arrival rate of workloads.

### Weakness

### TODO
1. Read detail theory proof if you are interested.

### Extension
1. This paper only considers the response time. How about also taking into account the profits? i.e., make the objective as a mix function of response time and revenue.
2. The workloads used in this paper are real, i.e., they are real jobs to be executed rather than job information.
