## [A Survey on Geographic Load Balancing Based Data Center Power Management in the Smart Grid Environment](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6578864&tag=1)

- reading status: 10/24/2014 ing



### Future work
#### Distributed Optimization Framework
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: All necessary information cannot be collected in a single point. Thus the front-ends do not have a global view of the entire workload of the system. 
- **Future direction**: the most effective power management should be decentralized in nature, so that it can be implemented at the different parts of the network coordinating through synchronous message passing.


#### Demand Profile Shaping
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: 
  - The workload fluctuates overtime due to the following 2 reasons
    - electricity price fluctuate overtime
    - typical internet service fluctuates overtime, e.g., the popular Internet application Windows Live Messagers exhibits a fluctuation of about 40% of the peak load within a day [[Chen-2008]](http://dl.acm.org/citation.cfm?id=1387613)
  - Thus, there are two problems
    - lower peaks and smooth the demand profile
    - turn on/off server, note repeated on-off cycles cause more wear-and-tear of various components of the server such as disks or fans and incur associated cost for their procurement and replacement; also bring a server to ON state from OFF state requires a considerable amount of time which affects QoS parameters like service delay.
- **Future direction**: there are two ways to tackle this problem
  - consider both price diversity and workload diversity, and make the objective of GLB as a function of both electricity cost and workload fluctuation; In particular, consider a reward function which is strictly decreasing in percentage of workload fluctuation
  - add constraints to bound workload variance within some tight limit

#### Data-intensive workload
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: Data-intensive workload such as HDFS requires the data availability, thus migration could be a problem.  Thus we need to consider the network congestion. 

#### Price Equilibrium
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: Data center is a large energy consumer, thus their schedule of workload can affect the power prices. Thus there exist a vacious cycle. i.e., Data center schedule the workload to consume current relative cheap energy price, and due to their large workload demand, power price increases. As a result, the price levels can tend to oscillate and some times turn to be unacceptably high.

#### Provisioning economic incentives to cloud computing clients
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: Cloud computing service charges are static, but the electric cost paid by the cloud computing operator is dynamic. 
- **Future work**: An effective cost reduction can be achieved by relaying this electricity price variability to cloud customers and making cloud operator pricing scheme dynamic.
  - More specifically, the service providers can also adopt real time pricing policy for their users and set variable service rates based on the electricity price they need to pay in the wholesale market.
    - Although a dynamic pricing scheme for cloud computing has been proposed in [[Buyya-2009]](http://www.sciencedirect.com/science/article/pii/S0167739X08001957), the proposed mechanism dos not consider the electricity price volatility within the smart grid. 

#### Hedgeing and Workload forecast
- Ref: [[Rahman]](https://github.com/hxwang/GreenDC-Summary/blob/master/papers/RahmanLK14_Survey-Geo-LoadBalancing.md)
- **Observation**: By hedging, the data center operators can purchase a certain amount of electricity beforehand to reduce unknown cost risks arising from the workload dynamics. 
- **Future direction**: However, it still remain open how to profitably hedge if the future workload volume cannot be estimated accurately. 
  - A natural direction is to combine hedging and load distribution together to achieve overall profit. The combined approach at first needs to decide on the appropriate amount of electricity to be pruchased for a future date at each data center and then ensure full use of the purchased amount of that date by adding appropriate workload constraints in the GLB's optimization framework.

#### Coordinate of Smart Grid and Data Center
- **Observation**: Currently GLB's benefit is one dimentional-- it passively monitors the smart grid for price-differentials to reduce costs in favor of data center operators. 
- **Future direction**: consider how to exploit GLB to potentially achieve efficiency of smart grid. How to coordinate interactions of power producers and massive power consumers like data center operators is till an unanswered question and this area needs more attention from the research community.

  

### Skipped for now
- Page 224, Joint content and network management
- Page 224, Dynamic application hosting management
- Page 227, Delay constraint modeling, `good`
