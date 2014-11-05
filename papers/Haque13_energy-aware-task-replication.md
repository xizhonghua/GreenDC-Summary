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

### Weakness

### Possible Extensions

### Check
- how to define the level of reliability
  - it defines as all timing constraints are met.
  - the reliability is defined as a function of frequency.
- further check how they use the reliability and frequency function.
- how to define the energy cost of replicaiton? Different task may have different energy consumption
- when the check of the error is conducted?
  - if the check is conducted too late and it shows the task has errors, then will the task miss its deadline if it has no time to be re-executed again?
