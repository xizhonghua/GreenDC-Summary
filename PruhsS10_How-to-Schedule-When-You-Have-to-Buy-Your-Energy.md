How to Schedule When you Have to Buy Your Energy
------

- [paper link](http://link.springer.com/chapter/10.1007%2F978-3-642-15369-3_27#page-1)
- bib
```
@article{
	author={Pruhs, Kirk and Stein, Cliff},
	title={How to Schedule When You Have to Buy Your Energy},
	booktitle={Approximation, Randomization, and Combinatorial Optimization. Algorithms and Techniques},
	year={2010},
    volume={6302},
	series={Lecture Notes in Computer Science},
	pages={352-365}
}
```
- version 1.0, last updated 09/11/2014

### Summary
This paper investigates how to maximize profits in a data center which consisting of speed-scalable processors. The revenue of a job is a function of how long the job is delayed. Each unit of energy has a fix cost. They give a (1+\epsilon) )O(1)-competitive algorithm, and show that resource augmentation is necessary to achieve O(1)-competitive.


### Model
- Machine: identical speed-scalable processors.
- Profits: lost as a function of how long the job is **delayed**,i.e., the revenue of finishing a job is denoted as I(t), which specifies the revenue that is obtained if the job is finished at time t.
- Energy: has fixed cost.
- Job: has released time r_i, known size w_i, and known revenue function
- Preemption: allowed
- Migration: allowed
- Objective: maximize profits, by determine which jobs to run on which processors, and at what speed to run the processors.

