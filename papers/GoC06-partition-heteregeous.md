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
In this paper, the authors investigate the problem of task partitioning on hegeregenous processors with replicas. They first prove the problem is NP hard in the strong sense by reducing it to the 3-PRTITION problem. And then, by using the properties of linear programming, they show existing approach(Baruah's approach) is difficult to be applied to solve this problem. As a result, they develop a Fully Polynomial-Time Approximation Scheme (FPTAS) to solve this problem.

### Strongness
- This paper is well written. The structure is very clear and the technical terms are explained in a way that is easy to understand.
- The authors analyze the reason that Baruah's arppaoch is diffcult to be applied in this problem model by using the properties of linear programming. The underlying reason is that the restriction that two replicas cannot be applied to the same processor makes the complexity of this problem grow exponentially.
- It seems the techniques (smallest quantum) used in the designed dynamic programming is similar to the one in book "Introduction to Algorithms (3rd)" page 1128, which introduces a fully polynomial-time approximation scheme for the subset-sum problem. 

### Weakness

### Possible Extensions
- Extend the problem model by taking the communication overhhead into account. As the authors mentioned, in this paper, they assume jobs are independent and neglect the communication overhead.
- Consider jobs that are of different importance and thus are associated with different number of replicas.

### Questions
- In the abstract, "no two replicas of the same task are assigned to the same processing unit", here "same processor unit" means "same processors" or "same processing time units"? I suppose it refers "same processors". 