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
This paper investigates how to maximize profits in a data center which consists of speed-scalable processors. The revenue of a job is a function of how long the job is delayed. Each unit of energy has a fix cost. They give a (1+&epsilon;) O(1)-competitive algorithm, and show that resource augmentation is necessary to achieve O(1) competitive ratio. 

- Theoretical summary
    - [PDF version](../algorithms/file/tex/Pruhs10-resourceAug.pdf)
    - [Latex version](../algorithms/file/tex/Pruhs10-resourceAug.tex)
    
### Model
- **Machine**: m identical speed-scalable processors.
    - power function P(s): specifies the power when a processor is run at speed s.
- **Energy**: has fixed cost.
- **Job**: 

|notations| meaning|
|:--------|:-------|
|r<sub>i</sub>| released time |
|w<sub>i</sub>| size|
|I<sub>i</sub>(t)|revenue function: the revenue that is obtained if the job is finished at time t.|
|preemption | allowed|
|pigration| allowed|
|parallel| a job can run on at most one machine at a time|

- **Objective**: maximize profits, by determine which jobs to run on which processors, and at what speed to run the processors.


### Question
- For the job settings, it seems there is no deadline, we only have the revenue function  I<sub>i</sub>(t) which has value 0 when t approximates infinity.
- For the job settings, it seems that a job only requires one machine node at a time, i.e., it is not parallel job.
- What is the running time of checking whether a job could have positive income? You might get it from Lemma 1.
    
### Comments
- Since for each job the revenue function I<sub>i</sub>(t) is irrelavant to the size of the job, thus this scheduling problem is equivalent to weighted jobs scheduling.

### Minor error
- In page 356, "integrated over all the times ~~the~~ that job is run"

### TODO
- reading section 4.2-4.4
- ref[21] [[Kalyanasundaram-2000]](http://www.sciencedirect.com/science/article/pii/S0196677400911283) introduces how to convert an optimal algorithm to a non-migrationary algorithm by increasing the number of processors by 6 times
