## Task Partitioning with Replication upon Heterogeneous Multiprocessor Systems

- reading status: started on 12/02/2014, finished on TBD
- bib
```
@inproceedings{GopalakrishnanC06,
 author = {Gopalakrishnan, Sathish and Caccamo, Marco},
 title = {Task Partitioning with Replication Upon Heterogeneous Multiprocessor Systems},
 booktitle = {Proceedings of the 12th IEEE Real-Time and Embedded Technology and Applications Symposium},
 series = {RTAS},
 year = {2006},
 pages = {199--207},
 numpages = {9}
} 
```

### Summary
In this paper, the authors investigate the problem of task partitioning on hegeregenous processors with replicas. The problem is NP hard in the strong sense. And they develop a Fully Polynomial-Time Approximation Scheme (FPTAS) for this problem.

### Strongness
- This paper is well written. The structure is very clear and the technical terms are explained in a way that is easy to understand.

### Weakness

### Possible Extensions
- Extend the problem model by taking the communication overhhead into account. As the authors mentioned, in this paper, they assuming jobs are independent and neglect the communication overhead.


### Questions
- In the abstract, "no two replicas of the same task are assigned to the same processing unit", here "same processor unit" means "same processors" or "same processing time units"? I suppose it refers "same processors". 
