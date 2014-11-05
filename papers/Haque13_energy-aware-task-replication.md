## [Energy-aware task replication to manage reliability for periodic real-time applications on multicore platforms](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6604518&tag=1)

- reading status: 11/04/2014 ing
- bib
```
@INPROCEEDINGS{HaqueAD13, 
  AUTHOR={Haque, M.A. and Aydin, H. and Dakai Zhu}, 
  BOOKTITLE={Green Computing Conference (IGCC), 2013 International}, 
  TITLE={Energy-aware task replication to manage reliability for periodic real-time applications on multicore platforms}, 
  YEAR={2013}, 
  PAGES={1-11}
}
```

### Summary
In the paper, the authors investigate the problem of how to achieve a target reliability for a set of periodic real-time applications with minimum energy consumption in DVS-enabled multcore systems. In specific, they show the general problem is intractable and propose an EER approximation algorithm. 
- Their simulation results demonstrate that the proposed mechanism could guarantee a wide range of reliability with minimum energy consumption by tuning the number of replications. `Rewrite this sentence`.

### Strongness
- Novelty
  - Previous works only focus on the reliability-oriented energy management on single-processor this paper. In this paper, the authors study this problem in terms of multicore system. In specific, multicore systems are more suitable for using replication for reliability management as there are more cores available to run the replicated tasks.
- The style of writing is very clear.
  - The authors first study with simplified models such as single task to convey the idea, give the definition and explain the phenomenon in a very clear way. This approach is more beneficial to the readers compare with the other style of writings which formulate the complicated problem as a whole at the very begining.
  
### Weakness
- Example 1 demonstrates that the energy consumption function, as a function of processing frequency, is neither convex and concave. The objective of the authors to show this example is to claim that no simple technique can be used to find the optimal configuration.
  - I am not sure whether it is enough to persuade the readers of the following techniques the author used. In specific, they use exhaustive search to get the ERF table with some further truncation. Maybe, we can further explore the equations (3)(4) to find other more efficient approach.
- In comparing the performance of exhaustive search and uniform frequency assignment, it is not mentioned about the comparison of the time cost.

### Possible Extensions
- Investigate the same problem while allowing the replicas to be executed using non-uniform frequencies.
  - It seems one more phase of energy reduction can be conducted after fixing the number of replicas. In specific, we can adjust the frequencies of replicas in pairs, i.e., replace a pair of uniform frequency to a non-uniform one by using one round of exhaustive search. 
  - However, note that this exhaustive search is different from the optimal exhaustive search which has two search dimensions, i.e., frequencies and number of replicas.

### To Check
- further check how they use the reliability and frequency function.
- how to define the energy cost of replicaiton? Different task may have different energy consumption
- when the check of the error is conducted?
  - if the check is conducted too late and it shows the task has errors, then will the task miss its deadline if it has no time to be re-executed again?
- how to partition the set of replicas among different cores?
- what is the time cost and energy cost of the algorithm?

### Checked
- how to define the level of reliability
  - it defines as all timing constraints are met.
  - the reliability is defined as a function of frequency.
