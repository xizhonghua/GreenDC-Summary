## Simulation setup of data center machines power consumption

### Example: [[Chen-2012]](../papers/ChenHT12-greenAware-geo-schedule.md)
Our simulated data centers are configured wit hteh same setting as previous studies[[Greenburg-2008]](http://dl.acm.org/citation.cfm?id=1496103), [[Le-2011]](http://dl.acm.org/citation.cfm?id=2063413).
- Each data center has the same Power Usage Efficienc (PUE), i.e., the total energy consumed by all facilities of the data center divided by the energy consumed by IT equipments. 
- We assume an inter-dta-cener bandwidth of 464 Mbps.
- Each data center contains 480 servers, each of which has 4 cores and 4GB memeory and can host at most four single-core virtual machines. 
- Our simulator accounts for the energy consumption at different states (idle, active and ACPI S3). 
- Sincethe resource allocation is at the granularity of virtual machines, we use the number of cores to approximate the machine utilization. Suppose the number of allocated cores is c. We estimate the power consumption ofr a machine to be P = base + c/total number of core *(peak - base), where the peak power and the base power are set to 300W and 200W, respectively. Thus P = 200 + 25c in our simulation. 
- The power consumption of ACPI S3 is 8.6W, and transiting into and out of S3 takes 7 seconds.
