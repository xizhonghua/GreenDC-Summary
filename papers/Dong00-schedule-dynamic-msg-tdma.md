## [Scheduling algorithms for dynamic message streams with distance constraints in TDMA protocol](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=854012&tag=1)

- reading status: start 11/06/2014, finished 11/11/2014
- bib
```
@INPROCEEDINGS{DongMM00, 
  AUTHOR = {Libin Dong and Melhem, R. and Mosse, D.}, 
  BOOKTITLE = {In proceedings of the 12th Euromicro Conference on Real Time Systems}, 
  TITLE = {Scheduling algorithms for dynamic message streams with distance constraints in TDMA protocol}, 
  YEAR = {2000}, 
  PAGES = {239-246}
}
```

### Summary
In this paper, the authors propose a real-time message model with both **rate requirements** and **distance constraints**. The authors first present a **dynamic\_greedy** algorithm which is efficient and local optimal, but might have larger jitter and low acceptance ratio. Then the authors transform the original problem to an optimization problem aiming at reducing the scheduling jitters and improve the acceptance ratio. They convert the optimization problem to a graph problem with weighted ages, thus finding the shortest path is then equivalent to decreasing the scheduling jitters. The authors then proposed a **dynamic\_optimization** algorithm to solve the optimization problem. Simulations results demonstrate that dynamic\_optimization has slightly higher acceptance ratio than dynamic\_greedy approach, and the average jitters of dynamic\_optimization is much smaller than dynamic\_greedy.


### Merits
- The mapping of the maximum distance problem to the classical *pinwheel problem* is beautiful. This mapping better illustrates the distance constraint in the proposed problem model and explains why the problem model in this paper is more complicated than *pinwheel problem*.
- The transformation of the optimization problem to a graph problem is fantastic! Particularly, by assigning weight to edges, they convert the problem of decreasing of scheduling jitter problem to finding shortest path problem. 

### Weakness
- No optimal offline algorithms are presented. Thus it might be hard to know how good is the performance of the online algorithms. The offline problem is that assuming the set of messages arriving are known beforehand, then what is the optimal algorithm that can improve the acceptance ratio while decrease the scheduling jitters?
- In the simulation, why the authors compare their online algorithms with EDF, why not compare with other algorithms. For example, a randomized algorithm which randomly assigns slots might be taken into account.
- In Fig.2, in the dynamic\_greedy algorithm,  instance\_needed  &le; k<sub>i</sub>, I think it should be "<" rather than "&le;"?
- It would be interesting to see the comparison of the real computation time of the proposed two algorithms. Because theoretical running time might not really corresponds to the performance in reality. Especially, the dynamic\_optimization algorithm needs some transformation which might introduce large time overhead.



### Possible Extensions
- When assigning a new message, it seems the authors did not take into account of future arriving message. Thus if we assume that messages are predictable, then how the performance can be further improved?
- The dynamic\_greedy algorithm might be improved by taking the scheduling jitters into account when assigning the remaining constants (line 9 in Figure 2).
- Consider the case when the bandwidth is not a constant, but varies over time.
- Taking into account of transmission failure. What if the transmission in some slot fails, and needs to be recovered as soon as possible.
- Consider the system is overloaded, and messages have different values, then how to decide the subsets of messages to accept and how to allocate slots to accepted messages?

### Questions
- In Fig.2, in the dynamic\_greedy algorithm,when instance\_needed  &le; k<sub>i</sub>, why randomly select other vacant slots rather than selecting with objective to minimize scheduling jitters?
- When convert the problem to graphic problem, what criteria do the authors use to assign the weight to edges and how do the weights corresponding to scheduling jitters

### Paper Contents
##### Motivation
- In real-time communication, **predictable** and **guaranteed timeliness** is one of the cirtical components of the quality of service (QoS) requirement.

##### Background
- Time Division Multiple Access (TDMA)
  - TDMA is a widely used protocol, where time is divided into equal length slots, each of which is equal to the transmission time of a message packet.
- Rate constraints
  - the proportion of time slots that should be assgined to a message stream.
- Distance constraints
  - the maximum timing interval between two adjacent instances.
  - e.g., The message stream in an Airborne Warning and Control System (AWACS) recording the position of an aircraft with a velocity of 900km/h may be subject to a distance constraint of 400 msecsm in order to ensure that the ground station obtains a positional accuracy of 100 meters.
- Scheduling jitter
  - defined as the variance of the distance between all neibouring instances of a message stream, must be low for a smooth servicing quality.

##### Model
- Each message stream is represented using M<sub>i</sub> = (A<sub>i</sub>, maxD<sub>i</sub>)

##### Comparison
- Algorithms
  - Dynamic approach v.s. Greedy approach
- Metrics
  - algorithm computational time
  - accept ratio of messages
  - scheduling jitter
  




