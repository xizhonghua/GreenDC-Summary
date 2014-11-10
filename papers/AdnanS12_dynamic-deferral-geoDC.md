[Energy Efficient Geographical Load Balancing via Dynamic Deferral of Workload](http://dl.acm.org/citation.cfm?id=2353793)
--- 

- reading status: 11/10/2014 ing
- bib
```
@inproceedings{AdnanS12
		author = {Adnan, Muhammad Abdullah and Sugihara, Ryo and Gupta, Rajesh K.},
		title = {Energy Efficient Geographical Load Balancing via Dynamic Deferral of Workload},
		booktitle = {Proceedings of the 2012 IEEE Fifth International Conference on Cloud Computing (CLOUD)},
		year = {2012},
		pages = {188--195},
		numpages = {8}
} 
```

### Summary
In this paper, the authors study the problem of workloads schedule among geographic data centers aiming at minimizing cost while meeting deadlines.
- They present an offline formulation.
- They design an online algorithm to determine the assignment of worklod to data center. Simulation results demonstrated their proposed mechanism can achieve 20-30% cost-savings.

### Motivation
In cloud computing, each center of execution (data center) are usually located in different geographic locations which are often in different time zones. Due to the increase in cost of energy, the electric billing companies have different pricing rates for electricity at different locations and at different times of day.
- Hence, load balancing decisions should take into account of current time zones and locations of data centers during task assignment.

### Model
- Workloads
	- latency: bounded delay
	- migration: allowed, in order to improve the performance in case of prediction error.
	- at time t, the total work load arrive is L<sub>t</sub>
- Date centers
	- a large computing facility ("cloud"), consisting of n data centers
	- at time t, the total workload L<sub>t</sub> arrive at a central dispatcher from which load balancing decisionss are made.
	- assumption: workload cannot be stored at dispatcher, they need to be dispatched to the data center after the assignment of workload for each data cener is determined. `My comment: assign immediately when they arrive?`

### Online algorithm
- Two levels
	- dispatcher level: the dispatcher makes decision about the assignment of the incoming workload to data centers based on predicted future electricity price.
	- data center level: the data centers make decision on adjusting the execution of the workload in current and future time slots and the migration of workload between ata centers in case of prediction error.


### Simulation
- Comparison
	- Since there is no constant competitive ratio for online algorithm, the authors compare the online algorithm with one that without migraiton and and future electricity price prediction.

### PPT
- For motivation: draw a figure, mark different data centers of Amazon to show different prices, time zones, load balancing concept.


### To Check
- In page-188, the offline optimal algorithm is executed at every time slot? If yes, then the problem formualtion will be weak.
- In page-189, is the decomposition of the workload by time slot &tau; reasonable? How to guarantee the executing order of all pieces of a job?
- In page-189, the execution time after migration is the same?

### Extension
- Incorporate renewable energy in the model.
