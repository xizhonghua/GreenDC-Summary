## [How to Schedule When you Have to Buy Your Energy](http://link.springer.com/chapter/10.1007%2F978-3-642-15369-3_27#page-1)


- Status: ing 10/24/2014
- bib
```
@ARTICLE{PruhsS10,
    AUTHOR={Pruhs, Kirk and Stein, Cliff},
    TITLE={How to Schedule When You Have to Buy Your Energy},
    BOOKTITLE={Approximation, Randomization, and Combinatorial Optimization. Algorithms and Techniques},
    YEAR={2010},
    VOLUME={6302},
    SERIES={Lecture Notes in Computer Science},
    PAGES={352-365},
    NUMPAGES = {14}
}
```


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
- &beta


