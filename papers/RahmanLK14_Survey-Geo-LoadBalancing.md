## [A Survey on Geographic Load Balancing Based Data Center Power Management in the Smart Grid Environment](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6578864&tag=1)

- reading status: 10/24/2014 ing



### 1. Extension
#### 1.1 Decentralized nature
- **Current state**: most of the research assume that their proposed GLB solution is executed entrally as if all the necessary information can be collected in a single point.
- **Observation**: The centralized information may not always be available. Thus centralized solution is very difficult to select parameter values in real time.
  - e.g., The data centers may not owned by the same system, thus it is difficult to have the centeralized information.
  - e.g., The front-end elements, accepting client requests, are also geo-distributed and do not have a global view of the entire workload at the same time.
- **Extenstion**: The most effective powre management should be **decentralized** in nature so that it can be implemented at the different parts of the network coordinating through asynchronous message passing.

#### 1.2 Demand profile shaping
- **Observation**: 
- The amount of workload processed by data centers fluctuates rapidly over time.
  - electricity prices: when the electricity price various hourly or daily in the deregulated electricity market the optimization sceme executed at the front end elements assigns more fluctuating workload (aligned with the price) to different data centers. 
  - a typical Internet service fluctuates: e.g., popular Internet application Windows Live Messenger exhibits a fluctuation of about 40% of the peak load within a day.
- It is always cost-effective for the data center to leave as many servers active as necessary. 
  - However, due to the unpredictable fluctuation of workload, it is very difficult to predict the number of active servers needed at any time instance. 
  - Workload fluctuation also increase the frequency of ON-OFF server transitions. Repeated on-off cycles cause more wear-and-tear of various components of the server such as disks or fans and incur associated costs for their procurement and replacement.
  - Time and energy cost: bring a server from a server to ON state from OFF state.
- **Current State**: The power demand profile becomes full of short-lived high peaks which enforces smart grid to keep additional generating plants available in standby mode only to be used during these short periods.
- **Extension**: 
  
