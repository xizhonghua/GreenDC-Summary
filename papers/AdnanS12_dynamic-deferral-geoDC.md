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
##### Workloads
- latency: bounded delay


### PPT
- For motivation: draw a figure, mark different data centers of Amazon to show different prices, time zones, load balancing concept.


### To Check
- In page-188, the offline optimal algorithm is executed at every time slot? If yes, then the problem formualtion will be weak.

