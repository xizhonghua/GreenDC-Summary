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
In this paper, the authors investigate the problem of task partitioning on heterogeneous processors with replicas. They first prove the problem is NP hard in the strong sense by reducing it to the 3-PRTITION problem. And then, by using the properties of linear programming, they show existing approach (Baruah's approach) is difficult to be applied to solve this problem. As a result, they develop a Fully Polynomial-Time Approximation Scheme (FPTAS) to solve this problem.


### Strongness
- This paper is well written. The structure is very clear and the technical terms are explained in a way that is easy to understand.
- The authors analyze the reason that Baruah's approach is difficult to be applied in this problem model by using the properties of linear programming. The underlying reason is that the restriction that two replicas cannot be applied to the same processor makes the complexity of this problem grow exponentially.
- It seems the techniques (smallest quantum) used in the designed dynamic programming is similar to the one in book "Introduction to Algorithms (3rd)" page 1128, which introduces a fully polynomial-time approximation scheme for the subset-sum problem. The dynamic programming approach designed in this paper is very intesting to me.
- The novelty of this paper compared with previous work is their taking into account of the replication problem and the heterogeneity of the processors.
- The formulation of the integer programming is interesting, i.e., the original problem is feasible only if the modified problem (as in the integer programming) has objective value no larger than 1.

### Weakness
- Some simulation results will make the theory result in this paper be more vivid. For example, given a setting, what is the cost of running time. Although it seems running time is not very important factors as the partition algorithm may only need to execute for once.



### Possible Extensions
- Extend the problem model by taking the communication overhhead into account. As the authors mentioned, in this paper, they assume jobs are independent and neglect the communication overhead.
- Consider jobs that are of different importance and thus are associated with different number of replicas.
- As the authors mentioned, we can consider other constraints such as the memory limits of processors, or power consumption. 
- Still, cancellation may be applicable to the problem when a replica of a task has executed successfully. It seems cancellation will make the partioning problem an online problem. However, in order to meet the hard deadline, the possibility of cancellation will not help in accomodating more tasks, it can only be used for energy saving purpose etc.

### Questions
- I am not clear how the constraints in the integer programming could ensure that all tasks meet with their deadline. 

