Voltage and frequency scaling mechanisms
---

### Dynamic Frequency Scaling(DFS)
- a.k.a. Clock Throttling or T-states, is a technique to manage power by running the processor at a less-than-maximum clock frequency. 
- The dynamic power used by a processor is approximately the cube of the speed of the processor(this is called the cube-root rule for CMOS based processors 
[[Brooks-2000]](https://github.com/hxwang/GreenDC-Summary/blob/master/basic/BrooksB00_Power-aware-Microarchitecture-Design-and-Modeling-challenges-for-next-generation-microprocessors.txt) 
[[Mudge-2001]](https://github.com/hxwang/GreenDC-Summary/blob/master/basic/Mudge01_Power-A-First-Class-Architectural-Design-Constraint.md).

- Under DFS, the Intel's 3.0 GHz Woodcrest Xeon processors allow for 8 operating points which correspond to effective frequencies of 12.5%, 25%, 37.5%, 50%, 62.5%, 75%, 87.5% and 100% ofthe maximum server frequency [[Gandhi-2009]](https://github.com/hxwang/GreenDC-Summary/blob/master/Gandhi09_Optimal-Power-Allocation-in-Server-Farms.md).




