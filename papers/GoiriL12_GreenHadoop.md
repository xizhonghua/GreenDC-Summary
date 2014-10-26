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



### Weakness
- It is not clear how the exact time of bounded delay is set, the author mentioned that in their experiment, they set the bounded delay as one day, but why not use other length?
 - In the simulation, the authors study the impact of setting different bounded delay 6 - 12 hours. And deadline violations occur but no very seriously.
 - The deadline violation occurs when the scheduler delay scheduling jobs to daytime to consume green energy, while some largers jobs come at daytime.
 - But the bound they explore is still very limited. From Table 1, we can see that 59% of jobs may only need several seconds to several minutes(with maximum about 4) to complete. However, the mininum bounded delay studied is 6 hours.
- It is not clear why their proposed mechanism only delays the scheduling of jobs with relative lower priority (normal, low and very low), but not the jobs with very high and high priority.
- The author argued that it is advantagerous to move idle servers to down state with the cost of replicating the data blocks in the moved servers. One argument is that the replication of a data block is cheaper than the power consumption. But I think it may not always be the case, it will also depend on the size of the data blocks.
- it is not cleary how to decide whether a job is about to miss its deadline?

### Questions
- What is the cost of replicating data from servers that are to be set to down sate?
- The estimation is in scale of groups of jobs rather than a single job, why?
- what's the transmission energy cost?
- what's the cost of copying data from transmissioned cost?
- In algorithm pseudocode line 18, why reject jobs if some of the jobs in the waiting queue is not assigned any energy? We know that when there are still remaining jobs in the waiting queue not assiged energy, then it means the system is overloaded. But how long is the scheduled horizon, i.e., what size is the schedule window?
- In algorithm pseudocode line 3, how to set the latest start time?
- What's the length of the scheduling horizon?
- what's the length of the bounded delay?
- In the evaluation in Fig. 11 and 12, why not take into peak brown power charges into account?

### TODO
- check the difference betweeen jobs priority are all set normal and mixed priority
- check what if the utilization is larger than 56%
- check what if the prediction is not accurate
- check the portion of jobs that are rejected by different mechanisms
- why not simulate with different job arrival patterns?
- check the time overhead.

### Merits
- The design of the experiments. If they only compare the full version with Hadoop, then they may not be able to understand how many energy saving comes from each factor. However, by studying several variance of the designed mechanism GreenHadoop, the authors present very clear where the energy saving comes from and how each heuristics used in the designed mechanism make contribution. 
- They study a lot of impact foctors.

### Faults
- It seems that the full version of GreenHadoop save less brown energy cost than the varaince GreenVarPrices. This result not make sense. The reason is because when compare Hadoop with GreenVarPrices, pick power consumption charge is neglected. The right approach is to also include the peak power consumption charge. 
- In Fig. 14, it is not make sense to compare the green energy consumption and brown energy cost in this case. Because the number of jobs executed by Hadoop and GreenHadoop could be different. When utilization is 92%, I am doubt that they can still violate no deadlines as claimed in the paper.

### Solved questions
- In algorithm pseudocode line 22,23,24, there are many servers can be tranmissioned, how to select which one to transmit?
 - when transition active -> decommissioned: select the one with fewest data blocks
- How to set the internal deadline of jobs?
 - it is assumed all non-high-priority jobs have the same bounded delay.

### Extension
- Consider the same problem in a different version in which green energy is bank on battery or the grid itself.
- Investigate the tuning of power to tradeoff peak-power cost(using more energy at night) and expensive daytime brown energy cost.
- Design mechanism when jobs are not bounded-delayed. Give an example of why the proposed mechanism is not applicable in this case.
- Study the same problem with the objective to maximize revenue assume that completing each job before its deadline will gain some revenue.
