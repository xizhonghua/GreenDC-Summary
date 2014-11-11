## Dynamic Power Management(DPM)

### Definition
- System components are put to sleep/low-power states when they are idle [[Benini-2000]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=845896&tag=1), [[V. Devadas-2008]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4550778).

### Power consumption in different states
In [[Goiri-2012]](../../papers/GoiriL12_GreenHadoop.md), there are three states of machine
- active: executing 1-4 tasks consumes 100W, 115W, 130W and 145W
- decommission: consumes 75W
- down: cosumes 9W, static power

### Transition time
