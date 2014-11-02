## Example of Competitive Ratio with Resource Augmentation

### Example: SETF
- SETF is (1+&epsilon;)-speed (1+1/&epsilon;)-competitive in terms of average response
  - This illustrates a phenomenon that is common in many scheduling problems: there is an almost fully scalable algorithm even though there are no O(1)-competitive algorithms
  - THe intition behind this is that if a system's load is near its cpacity, then the online scheduler has no time to **recover from even small mistakes**. 
  - Many of the strong worst-case lower bounds for online scheduling problems utilize input instance where the load is essentially the capacity of the system.


### Example: SPRT
- Model: there are m identical servers. No jobs can run simultaneously on more than one server.
- It is shown that SPRT is a (1-1/m)-speed 1-competitive algorithm for minimizing total response time on parallel servers [[Phillips-2002]](http://dl.acm.org/citation.cfm?id=258570).


### Example: HDF
- Highest Density First(HDF)
- [[Becchetti-2001]](http://link.springer.com/chapter/10.1007%2F3-540-44666-4_8#page-1) proves that HDF is (2+&epsilon;)-speed O(1) competitive.

### Example: RR
- [[Edmonds-2000]](http://dl.acm.org/citation.cfm?id=301299) proves that Round Robin(RR) is (2+&epsilon;)-speed O(1)-competitive. 
