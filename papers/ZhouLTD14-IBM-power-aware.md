## [Reducing Energy Costs for IBM Blue Gene/P via Power-Aware Job Scheduling](http://link.springer.com/chapter/10.1007%2F978-3-662-43779-7_6#)

- reading status: start 11/12/2014, finished on 11/12/2014
- bib
```
@incollection{ZhouLTD14
year={2014},
booktitle={Job Scheduling Strategies for Parallel Processing},
series={Lecture Notes in Computer Science},
title={Reducing Energy Costs for IBM Blue Gene/P via Power-Aware Job Scheduling},
author={Zhou, Zhou and Lan, Zhiling and Tang, Wei and Desai, Narayan},
pages={96-115}
}
```

### Summary
In the paper, the authors study the problem of reducing energy cost at high-performance computing (HPC) systems. They consider the dynamic electricity price, jobs power profile and energy capping. By using scheduling windows, they guarantee the fairness of jobs and form the problem into a 0-1 knapsack problem. The idea is to schedule low power-intensive jobs when electricity price is high, i.e., maximize the number of nodes used (guarantee system utilization) while meeting the power budget constraints.

### Problem Model
- scheduling window: to guarantee fairness
  - They use a window-based scheduling mechanism to avoid breaking the fairness of job scheduling as much as possible. Rather than allocating jobs one by one from the front of the queue as adopted by existing schedulers, their method allcoates a window of jobs at a time. The selection of jobs into the window is to guarantee certain fairness, while the allocation of the jobs in the window onto system resources is to meet our objective of maximizing system utilization without exceeding the predefined power budget.
  - rather than allocate jobs one by one from the wait queue, our scheduler makes decisions on a group of jobs selected from the waiting queue.
- jobs
  - with power profiling
- schedule problem
  - How can we schedule jobs with different power profiles, without exceeding a predefined power budget and at the same time not affecting system utilization and not breaking the fairness of scheduling as much as possible?
  - i.e., **0-1 Knapsack Model**, given a set of jobs and the required node of each job, the objective is to find the subset of jobs to execute to maximize the number of nodes used with the energy budget constraint.


### Scheduling algorithm
- When the electricity price is high, in order to save energy costs, they reduce the total amount of powre demand consumed by the jobs allocated on the system.


### My comment
- Note that they only apply their algorithms in the on-peak periods. The idea is to reduce the power consumption density of jobs, so as not to hurt the utilization as well as use as less energy as possible,


### Questions
- They didn't mention the length of a job. So do they assume that each job can be finished in exactly one scheduling window? Otherwise, if jobs have different execution time, it seems this mechanism will not work.

### Skip for now
- Section 4: simulation results analysis

### Extension
- Integrate renewable energy.
