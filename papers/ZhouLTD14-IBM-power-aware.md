## [Reducing Energy Costs for IBM Blue Gene/P via Power-Aware Job Scheduling](http://link.springer.com/chapter/10.1007%2F978-3-662-43779-7_6#)

- reading status: start 11/12/2014
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


### Problem Model
- scheduling window: to guarantee fairness
  - They use a window-based scheduling mechanism to avoid breaking the fairness of job scheduling as much as possible. Rather than allocating jobs one by one from the front of the queue as adopted by existing schedulers, their method allcoates a window of jobs at a time. The selection of jobs into the window is to guarantee certain fairness, while the allocation of the jobs in the window onto system resources is to meet our objective of maximizing system utilization without exceeding the predefined power budget.
  - rather than allocate jobs one by one from the wait queue, our scheduler makes decisions on a group of jobs selected from the waiting queue.
- jobs
  - with power profiling
- schedule problem
  - How can we schedule jobs with different power profiles, without exceeding a predefined power budget and at the same time not affecting system utilization and not breaking the fairness of scheduling as much as possible?
  - i.e., **0-1 Knapsack Model**, given a set of jobs and the required node of each job, the objective is to find the subset of jobs to execute to maximize the number of nodes used with the energy budget constraint.
