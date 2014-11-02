## Definition of Resource Augmentation

### Definition
- An online algorithm A is an s-speed c-approximation algorithm if
  - max<sub>I</sub> A<sub>s</sub>(I) / Opt<sub>1</sub>(I) &le; c
    - A<sub>s</sub>(I): the QoS measure of the schedule produced by algorithm A with a speed s server on input I
    - Opt<sub>1</sub>(I): the optimal QoS value achivable on a unit speed server
- (1+&epsilon;)-speed augmentation
  - it means if a processor can run at power P and speed s, then the online algorithm can run the processor at power p and speed (1+&epsilon;)s.
  - This is essentially the best possible resource augmentation result that one can obtain, called **almost fully scalable** algorithm.
