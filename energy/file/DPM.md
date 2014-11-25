## Dynamic Power Management(DPM)

### Definition
- System components are put to sleep/low-power states when they are idle [[Benini-2000]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=845896&tag=1), [[V. Devadas-2008]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4550778).


### When to set server to sleep mode
- [[Gandhi-2012]](http://dl.acm.org/citation.cfm?id=1555349.1555368) Timeout policy: if a server has been in idle state longer than a timeout threshold, i.e., T<sub>out</sub>, then it automatically sleeps. A good threshold could be: T<sub>out</sub> = T<sub>up</sub> * P<sub>max</sub> / P<sub>idle</sub>, where T<sub>up</sub> is the server walking up time, P<sub>max</sub> is the power consumption during waking up period, which equal to the maximum, and P<sub>idle</sub> is the server idle power. 

