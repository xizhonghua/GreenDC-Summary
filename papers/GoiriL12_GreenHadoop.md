## [GreenHadoop: Leveraging Green Energy in Data-Processing Frameworks](http://dl.acm.org/citation.cfm?id=2168843)

- reading status: ing 10/25/2014
- bib
```
@INPROCEEDINGS{GoiriLNGTB12,
 AUTHOR = {Goiri, \'{I}\~{n}igo and Le, Kien and Nguyen, Thu D. and Guitart, Jordi and Torres, Jordi and Bianchini, Ricardo},
 TITLE = {GreenHadoop: Leveraging Green Energy in Data-processing Frameworks},
 BOOKTITLE = {Proceedings of the 7th ACM European Conference on Computer Systems(EuroSys)},
 YEAR = {2012},
 PAGES = {57--70}
 NUMPAGES = {14}
} 
```

### Summary 
In this paper, the authors investigate how to manage a datacenter's computational workload to match the green energy supply in small/medium datacenters running data-processing frameworks. Their objective is schedule the MapReduce jobs to maximize the green energy consumption within jobs' time bounds. The experimental results demonstrate that their proposed mechanism could increase green energy consumption and decrease electricity cost, compared to Hadoop. The main idea is
- delay some jobs to wait for available green energy
- if borwn energy must be used, they will pick the cheapest time, while also managing the cost of peak brown energy consumption
- in specific, it will also decide how many servers to use, and it transitions other servers to low-power states to the extent possible.

### Model
- Settings
 - no battery
 - jobs have bounded delay, job energy requirement is estimated using historical data
 - brown energy price are dynamic
 - green energy can be predicted 
 
### Simulation 
- Settings
 - green energy: scaled-down version of an existing Rutgers solar farm
 - brown energy price: the dynamic brown energy price and peak brown power charges are from a power company in New Jersey
 - green data center: 16-server cluster
 - workloads: 2 realistic workloads
- Comparison
 - compare with standard hadoop
- Explore other effects?
 - check if they measure the case when the prediction is not accurate

### Strongness

### Weakness
- It is not clear how the exact time of bounded delay is set, the author mentioned that in their experiment, they set the bounded delay as one day, but why not use other length?
- It is not clear why their proposed mechanism only delays the scheduling of jobs with relative lower priority (normal, low and very low), but not the jobs with very high and high priority.
- The author argued that it is advantagerous to move idle servers to down state with the cost of replicating the data blocks in the moved servers. One argument is that the replication of a data block is cheaper than the power consumption. But I think it may not always be the case, it will also depend on the size of the data blocks.

### Questions
- What is the cost of replicating data from servers that are to be set to down sate?
- The estimation is in scale of groups of jobs rather than a single job, why?
- what's the transmission energy cost?
- what's the cost of copying data from transmissioned cost?
- In algorithm pseudocode line 18, why reject jobs if some of the jobs in the waiting queue is not assigned any energy? We know that when there are still remaining jobs in the waiting queue not assiged energy, then it means the system is overloaded. But how long is the scheduled horizon, i.e., what size is the schedule window?
- In algorithm pseudocode line 3, how to set the latest start time?
- What's the length of the scheduling horizon?
- what's the length of the bounded delay?


### TODO
- check the difference betweeen jobs priority are all set normal and mixed priority
- check what if the utilization is larger than 56%
- check what if the prediction is not accurate
- check the portion of jobs that are rejected by different mechanisms
- why not simulate with different job arrival patterns?

### Solved questions
- In algorithm pseudocode line 22,23,24, there are many servers can be tranmissioned, how to select which one to transmit?
 - when transition active -> decommissioned: select the one with fewest data blocks
- How to set the internal deadline of jobs?
 - it is assumed all non-high-priority jobs have the same bounded delay.

### Extension
- Consider the same problem in a different version in which green energy is bank on battery or the grid itself.
- Investigate the tuning of power to tradeoff peak-power cost(using more energy at night) and expensive daytime brown energy cost.
