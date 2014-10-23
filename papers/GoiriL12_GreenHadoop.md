## [GreenHadoop: Leveraging Green Energy in Data-Processing Frameworks](http://dl.acm.org/citation.cfm?id=2168843)

- reading status: haven't started
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
 
### Simulation Settings
- green energy: scaled-down version of an existing Rutgers solar farm
- brown energy price: the dynamic brown energy price and peak brown power charges are from a power company in New Jersey
- green data center: 16-server cluster
- workloads: 2 realistic workloads

### Strongness

### Weakness

### Extension
- Consider the same problem in a different version in which green energy is bank on battery or the grid itself.
