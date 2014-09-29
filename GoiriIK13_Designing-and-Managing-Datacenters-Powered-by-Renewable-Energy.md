[Designing and Managing Datacenters Powered by Renewable Energy](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6756707)
---

- Reading status
- finished v1 in 09/29/2014

- bib
```
@ARTICLE{6756707, 
author={Goiri, I and Katsak, W. and Kien Le and Nguyen, T.D. and Bianchini, R.}, 
journal={Micro, IEEE}, 
title={Designing and Managing Data centers Powered by Renewable Energy}, 
year={2014}, 
volume={34}, 
number={3}, 
pages={8-16}, 
}
```


### Summary
This paper introduced the designing of a green data center. In specific, it introduced the designed data center Parasol, and the management system GreenSwitch. In addition, it summarize the lessons learned in building up the datacenter.


### Parasol
- it is the **first** green data center prototype
- the designed green data center, each compoenents of the data center is introduced
- the cooling system works less than 1% of the time
- the green energy consumption trend in a long time period
- the data center's operation during hurricane Sandy demonstrate the potential for green datacenters to operate through **power outages** (or in remote locations without a reliable grid power source)

### GreenSwitch
- it is a system for scheduling workloads, selecting the source of energy to use(renewable, battery, and/or grid), and/or selecting the renewable energy storage medium(battery or grid) at each point in time.
- it seeks to minimize the overall cost of grid electricity (including both **grid energy** and **peak grid power**) while respecting the characteristics for the workload and battery lifetime constraints. 
- the simulation results show that GreenSwitch can transitioned many servers to sleep in the early hours of the day and deferred some of the load until solar energy was available. 
- compared to a grid-only datacenter, GreenSwitch produced a profit of 9% in grid electricty cost. Given this profit, GreenSwitch would amortize the cost of the solar stepup and batteries in only 7.6 years.

### Main Lessons
- placing Parasol on the roof of a building (instead of on the ground) prevented shading from other buildings. 

### Observations
- The energy losses (e.g., in power conversion) are highly dependent on load, rather than a fixed percentage as often assumed in simulation. 


### Simualtion 
- use [Facebook Trace](https://github.com/hxwang/Seminar/blob/master/Paper-Summary/traces/facebook-swim.md)

### Possible Extension
-  as pointed out in the paper, we can research on the interplay of solar energy and free cooling, since solar energy is most abundant when outside temperature is hottest
- as pointed out in the paper, we can research on the interplay of using renewable energy and using battery energy. (I am not very clear about this point right now.)
