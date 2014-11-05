## Dynamic Voltage and Frequency Scaling(DVFS) 

### Definition 
- a.k.a. P-states, is a more efficiency power-savings mechanism that reduces server frequency by reducing the processor voltage and frequency. 

### Shortage
- Current research suggests the negative impact of DVFS on the transient fault rate [[Ernst-2004]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1388152&tag=1), [[Zhu-2004]](http://dl.acm.org/citation.cfm?id=1112252): as we decrease the supply voltage and frequency to save power, the transient fault rate (and the corresponding soft errors) increase exponentially.
  - Therefore, energy management must take into account of the reliability degradation and make provisions accordingly [[Haque-2013]](../../papers/Haque13_energy-aware-task-replication.md).


