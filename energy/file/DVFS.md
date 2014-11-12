## Dynamic Voltage and Frequency Scaling(DVFS) 

### Intro
- DVFS is a widely used technique for controlling CPU power since the power consumption of processors occupies a substantial portion of the total system power (roughly 50% under load) [[Mammela-2012]](http://link.springer.com/article/10.1007%2Fs00450-011-0189-6#page-1) 
- DVFS enables a process to run at a lower frequency or voltage, increasing the job execution time in order to gain energy savings.


### Definition 
- a.k.a. P-states, is a more efficiency power-savings mechanism that reduces server frequency by reducing the processor voltage and frequency. 

### Shortage
- Current research suggests the negative impact of DVFS on the transient fault rate [[Ernst-2004]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1388152&tag=1), [[Zhu-2004]](http://dl.acm.org/citation.cfm?id=1112252): as we decrease the supply voltage and frequency to save power, the transient fault rate (and the corresponding soft errors) increase exponentially.
  - Therefore, energy management must take into account of the reliability degradation and make provisions accordingly [[Haque-2013]](../../papers/Haque13_energy-aware-task-replication.md).

### Exceptions
- [[Zhou-2014]](../../papers/ZhouLTD14-IBM-power-aware.md) DVFS is not appropriate for some HPC systems. For example, DVFS is both less feasible and less important for the blue gene series because it dose not include comparable infrastructure and already operates at highly optimized voltage and frequency ranges [[Hnnecke-2012]](http://link.springer.com/article/10.1007%2Fs00450-011-0192-y#page-1). Green Density [[Feng-02]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1137753) are build based on low frequency process to achieve the goal of energy efficiency which leaves little space for DVFS which performs better on systems equipped with high frequency processors. 

