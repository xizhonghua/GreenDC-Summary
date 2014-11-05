## [Energy-aware task replication to manage reliability for periodic real-time applications on multicore platforms](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6604518&tag=1)

- reading status: finished 11/05/2014
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
In the paper, the authors investigate how to use replication to achieve a target reliability for a set of periodic real-time applications in DVS-enabled multicore systems with minimum energy consumption. In specific, they show the general problem is intractable and propose an EER approximation algorithm. Their simulation results demonstrate that the proposed mechanism is much more energy efficient than the baseline approach which runs at the maximum CPU frequency.

### Merits
- Novelty
  - Previous works only focus on the reliability-oriented energy management on single-processor this paper. In this paper, the authors study this problem in terms of multicore system. In specific, multicore systems are more suitable for using replication for reliability management as there are more cores available to run the replicated tasks.
- The style of writing is very clear.
  - The authors first study with simplified models such as single task to convey the idea, give the definition and explain the phenomenon in a very clear way. This approach is more beneficial to the readers compare with the other style of writings which formulate the complicated problem as a whole at the very beginning.
  
### Weakness
- In the mathematic formulation of the GEERP problem in page 7, it seems it lacks one constraint of &tau;<sub>m</sub>, i.e., there is no constraint saying that each replicas of &tau;<sub>i</sub> should be assigned to a core. Although obviously the authors have taken this into account.
- Example 1 demonstrates that the energy consumption function, as a function of processing frequency, is neither convex and concave. The objective of the authors to show this example is to claim that no simple technique can be used to find the optimal configuration.
  - I am not sure whether it is enough to persuade the readers of the following techniques the author used. In specific, they use exhaustive search to get the ERF table with some further truncation. Maybe, we can further explore the equations (3)(4) to find other more efficient approach.
- In comparing the performance of exhaustive search and uniform frequency assignment, it is not mentioned about the comparison of the time cost.
- There is no comparison with the optimal algorithm.

### Possible Extensions
- Investigate the same problem while allowing the replicas to be executed using non-uniform frequencies.
  - When consider only one task, it seems one more phase of energy reduction can be conducted after fixing the number of replicas. In specific, we can adjust the frequencies of replicas in pairs, i.e., replace a pair of uniform frequency to a non-uniform one by using one round of exhaustive search. 
  - However, note that this exhaustive search may not be optimal and is different from the optimal exhaustive search which has two search dimensions, i.e., frequencies and number of replicas.
- Replicas may be scheduled to execute at different cores at different time periods (reduce the overlap in time), thus wheneve a replica of a task is finished successfully, then we can abandon the other replicas of the task.


### Checked
- how to define the level of reliability
  - the reliability is defined as a function of frequency.
- further check how they use the reliability and frequency function.
  - use to determine the frequency required to guarantee reliability.
- how to define the energy cost of replicaiton? Different task may have different energy consumption
  - energy is defined as a function of frequency
- how to partition the set of replicas among different cores?
  - use the known heuristic
- what is the time cost and energy cost of the algorithm?
  - since this algorithm is run only once and can be precomputed, thus the overhead of time and energy cost is not important.
