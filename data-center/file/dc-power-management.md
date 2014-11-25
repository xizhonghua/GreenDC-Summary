## Data Center Power Management

- courtesy of [[Chen-2014]](papers/Chen14-IGCC-participate-in-grid.md).

### 1. Power Budget
- Some power budgeting approaches consider the heterogenous set of applications and divide total power caps based on application peroperties [[Rajamani-2006]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4086132&tag=1) [[Zhan-2013]](http://dl.acm.org/citation.cfm?id=2488951).

### 2. Job Scheduling
- Job scheduling impacts the power and performance of dta centers, and therefore, has been extensively studies. First-in first out (FIFO) policy is widely used strategy today because of its simplicaity and fairness. Back-filling is another popular strategy aiming to improve system utilization [[Mualem-2001]](http://dl.acm.org/citation.cfm?id=380315).

### 3. Server Provisioning
- Server provisioning, which decides how many servers should be avtive at a given time, is another essential topic in the data center. 
- Many data centers today leave all the unused servers in idle states as a conservative approach for guranteeing high performance. Leaving many servers idle, however, causes tremendous waste of energy. Some data center reseraches leverage sleep states to improve energy efficiency [[Chase-2001]](http://dl.acm.org/citation.cfm?id=502045) [[Nathuji-2008]](http://link.springer.com/article/10.1007%2Fs10586-008-0054-y#page-1). However, they typically ignore the wake-up costs from sleep states or use hypothetical server states. [[Gandhi-2012]](http://dl.acm.org/citation.cfm?id=2410779) propose a SoftReactive dynamic power management policy, which determines the state of servers in the data center based on the dynamic workload arrival rate, and introduce a timeout-based mechanism to sleep servers.


### 4. Data Center Demand Response Programs and Strategies
While data center energy costs can be reined in by improvmenets in energy efficiency, demand response to spatio-temporally varying system costs adnd capacity reserve needs is emerging as an even more effective money saver.  We review the following to programs
- Legacy demand response
  - Peak shaving
  - Interruptible load contracts
  - Load Shedding and shifting across time
- New demand response programs that are emerging from the participation of loads in power markets on par with generation side participants. 
  - The primary, secondary and tertiary capacity reserves by loads

##### 4.1 Peak Shaving
- Since the peak-power charge could be high, thus data centers often use power capping, DVFS or leverage on workloads migration in geographical data centers to shae peak power usage. 

- [[Zois-2014]](../../papers/ZoisFCSP14-customer-selection-smart-grid.md): Installing additional power generation capability to meet peak demands sometimes is neither feasible nor sufficient. Demand Response (DR) [[Albadi-2007]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4275494) is a well known method employed by energy providers to control demand. It is used to find the equilibrium between energy prediction and demand through load control.


### 5. Load shedding, Shifting and Migration
