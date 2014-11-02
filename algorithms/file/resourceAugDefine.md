## Definition of Resource Augmentation

### Definition
- An online algorithm A is an s-speed c-approximation algorithm if
  - max<sub>I</sub> A<sub>s</sub>(I) / Opt<sub>1</sub>(I) &le; c
    - A<sub>s</sub>(I): the QoS measure of the schedule produced by algorithm A with a speed s server on input I
    - Opt<sub>1</sub>(I): the optimal QoS value achivable on a unit speed server
- (1+&epsilon;)-speed augmentation
  - it means if a processor can run at power P and speed s, then the online algorithm can run the processor at power p and speed (1+&epsilon;)s.
  - This is essentially the best possible resource augmentation result that one can obtain, called **almost fully scalable** algorithm.

### Example
- SETF is (1+&epsilon;)-speed (1+1/&epsilon;)-competitive in terms of average response
  - This illustrates a phenomenon that is common in many scheduling problems: there is an almost fully scalable algorithm even though there are no O(1)-competitive algorithms
  - THe intition behind this is that if a system's load is near its cpacity, then the online scheduler has no time to **recover from even small mistakes**. 
  - Many of the strong worst-case lower bounds for online scheduling problems utilize input instance where the load is essentially the capacity of the system.
