## Server State Transition

### Server State
- [[Power States]](http://en.wikipedia.org/wiki/Sleep_mode)

### Power consumption in different states
- In [[Goiri-2012]](../../papers/GoiriL12_GreenHadoop.md), there are three states of servers. Each server is a 4-core Xeon machine with 8GB RAM and 7200-rpm SATA disk with 64GB free space for data. 
	- active: executing 1-4 tasks consumes 100W, 115W, 130W and 145W
	- decommission: consumes 75W
	- down (ACPI S3 “Sleep” state): cosumes 9W, static power
- [[Raj-2012]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6151371)
![](../figs/powerStates.PNG)

### State transition time cost
- [[Raj-2012]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6151371)
![](..figs/transitionTime.PNG)

### State transition energy cost
