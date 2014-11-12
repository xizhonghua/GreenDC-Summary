Data Center CPU Utilization
---

### Overview
- [[Zhou-2014]](http://link.springer.com/chapter/10.1007%2F978-3-662-43779-7_6#page-1) Unlike Internet data centers that typically run at about 10-15% utilization, system at HPC centers have a typical utilization of 50-80% [[Parallel-workload-arhive]](http://www.cs.huji.ac.il/labs/parallel/workload/), and job queues are rarely empty because of the insatisfiable demand in science and engineering. Therefore, an approach is needed that can save energy cost while maintaining relatively high system utilization.

### Google server utilization
- [Ref](../file/BarrosoC13_The-Datacenter-as-a-Computer-An-introduction-to-design-of-warehouse-scale-machines.md)
- The figure below show three-month average utilization rates for 20,000 server clusters in Google. The typical cluster on the left spent most of its time running between **20-40 percent** of capacity, and the highest utilization cluster on the right reaches such heights only because it's doing batch work.
![](../figs/utilization-google-cluster.PNG)

### Amazon
- [Ref](http://huanliu.wordpress.com/2012/02/17/host-server-cpu-utilization-in-amazon-ec2-cloud/)
- The profile of a random server

![](../figs/ec2Util.PNG)

- The profile of the busiest server observed

![](../figs/ec2BusyUtil.PNG)
