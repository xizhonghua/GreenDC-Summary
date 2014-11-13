## [Scheduling to minimize gaps and power consumption](http://link.springer.com/article/10.1007%2Fs10951-012-0309-6)

- reading status: haven't started
- bib
```
```

### Summary
In this paper, the authors study the problem of tasks scheduling with the objective to minimize the power consumption and minimize the number of gaps. Each power can go to sleep at cost &alpha;. They design polynomial-time algorithm based on sophisticated dynamic programming for both objectives. 
- For power saving problem, they develp a (1+2/3&alpha;)-approximation algorithm, and show that dependence on &alpha; is necessary.
- For multi-interval gap scheduling problem, it is set-cover hard. They give an O(\sqrt(n))-approximation for maximizing throughput given a hard upper bound on the number of gaps.

### Motivation
- In sleep state, servers consume no power but disallows computation.
- However, each transition of sleep state to regular, active state consumes a fixed amount of power.
- So we cannot simply go to sleep whenever computation is not required.

### Problem Model
- Server
  - each server can go to sleep at cost &alpha;
- Job
- Objective
  - Power minimization: minimize the total transition costs plus the total time spent in the active state.
  - Gap scheduling: minimize the total number of transitions. `Comment: though minimizing total power is the most natural measure, minimizing the number of transitions (as in gap scheduling) seems stronger from the point of view of approxiamtion algorithm`.


### Question
1. In page 152, what does "where each job has one interval (arrival time and deadline)" mean?
