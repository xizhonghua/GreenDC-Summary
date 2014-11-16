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

### Electricity Price Prediction Model
- Challenge: Predicting electricity prices is difficult because price pesries present such characteristics as nonconstant mean and variance and significant outliers.
- Approach: Gaussian random varianbe
	- They model the prediction noise by a Gaussian random variable with zero mean and **estimated** variance.
	- The future price is odeled by Gaussian random varianble with known mean, which are predicted prices, and some estimated variance.
		- Mean: predicted using `moving average method`
		- Variance: estmated from the history by weighted average price prediction filter proposed in [[Mohsenian-Rad-2010]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5540263&tag=1)
- Prediction of variance: using `linear regression` from the previous prices from yesterday, the day before yesterday (temporal data) and the same day last week (historical data).
	- the coefficients for the moving average method can be estimated by training the model over previous say prices.
	

### Simulation
- Comparison
	- Since there is no constant competitive ratio for online algorithm, the authors compare the online algorithm with one that without migraiton and and future electricity price prediction.

### PPT
- For motivation: draw a figure, mark different data centers of Amazon to show different prices, time zones, load balancing concept.

### Weakness
- Migration may not be appropriate or must associate with non-negligible time cost for data-intensive jobs, e.g., MapReduce workloads.
- Online algorithm contains 2 steps. The first step is moving jobs to earlier time slots, and the second step is to migrate jobs to other data centers. By forming th problem as 2 steps, it simplifies the problem. However, it might not achieve economic cost. For example, by moving jobs earlier first, jobs might miss opportunity to migrate to other data centers which could achieve more cost savings.
- Consider data availability. In fact they assume migration time is negligible, which is not make sense when large data need to be migrated along with the job.
- In page 193, in proving of Theorem 5, they should repleace the prediction error as other parameters rather than &epsilon; , otherwise, it is rather confusing.

### To Check
- In page-188, the offline optimal algorithm is executed at every time slot? If yes, then the problem formualtion will be weak.
- In page-189, is the decomposition of the workload by time slot &tau; reasonable? How to guarantee the executing order of all pieces of a job?
- In page-189, the execution time after migration is the same?
- In page-191, why the prediction of the mean of electricity price is related to D?
- In page-191, the online optimization can only move jobs to earlier slots, but not later slots?
- In page-192, what does Equation 6 mean?
- In page-193, in the simulation, if D is uniform, the authors vary deadline D from 1-12. Note that in order to compare the performance of different algorithms, we need to ensure that these algorithms complete exactly the same set of jobs.
- Check if they consider the heterogenous reponse time of data centers
- check if the time overhead evaluated?

### Extension
- Incorporate renewable energy in the model.
- Incorporate heterogeneity.
- If jobs are not with uniform deadline, then the prediction of future arriving workload will also be important?

### TODO
- Page 192-193, read proof of Theorem 5.


### Typo
- In Page-189, "that is migrated form data center i to j", "form" -> "from"
