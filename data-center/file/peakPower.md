## Peak Power

### Peak power is harmful
- Massive electricity flow from smart grid to a data cetner may cause sudeen drop in voltage, sometimes even power outages. 
- Interesting, geographic load balancing(GLB) has potential to assist in correct operation of smart grid. 
  - e.g., GLB can reduce amount of workload to a data center where the smart grid is currently error prone.
  - e.g., gLB can also distribute service requests among data centers so that current is drawn uniformly from power grid and electric load balancing is ensured.
  - All of these techniques are of significance improtance to aid better design, load balancing and robustness of future smart grid.
  
### What's peak power price?
- Datacenter also have to pay for their peak brown energy consumption, i.e., dollar amount per kW of borwn power at the highest period of borwn power usage. 

### How to compute cost?
- To compute the peak charges, utilities typically monitor the average brown energy consumption within **15-minite windows** during each month. They define the maximum of these averages as the peak borwn power for the month.

### How large is peak power cost?
- Even though  these charges have almost always been overlooked in the literature, the peak brown power charge can be significant, especially during the summer. [[Govindan-2011]](http://dl.acm.org/citation.cfm?id=2000064.2000105) estimate that this component can represent up to 40% of the overall electricity cost of a datacenter.
