## [Scheduling algorithms for dynamic message streams with distance constraints in TDMA protocol](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=854012&tag=1)

- reading status: ing 11/06/2014
- bib
```
@INPROCEEDINGS{854012, 
  AUTHOR = {Libin Dong and Melhem, R. and Mosse, D.}, 
  BOOKTITLE = {Real-Time Systems, 2000. Euromicro RTS 2000. 12th Euromicro Conference on}, 
  TITLE = {Scheduling algorithms for dynamic message streams with distance constraints in TDMA protocol}, 
  YEAR = {2000}, 
  PAGES = {239-246}
```

### Summary
In this paper, the authors propose a real-time message model with both **rate requirements** and **distance constraints**. Two algorithms for scheduling dynamic real-time message streams in a TDMA frame are proposed and evaluated through simulations.


### Motivation
- In real-time communication, **predictable** and **guaranteed timeliness** is one of the cirtical components of the quality of service (QoS) requirement.


### Background
- Time Division Multiple Access (TDMA)
  - TDMA is a widely used protocol, where time is divided into equal length slots, each of which is equal to the transmission time of a message packet.
- Rate constraints
  - the proportion of time slots that should be assgined to a message stream.
- Distance constraints
  - the maximum timing interval between two adjacent instances.
  - e.g., The message stream in an Airborne Warning and Control System (AWACS) recording the position of an aircraft with a velocity of 900km/h may be subject to a distance constraint of 400 msecsm in order to ensure that the ground station obtains a positional accuracy of 100 meters.
- Scheduling jitter
  - defined as the variance of the distance between all neibouring instances of a message stream, must be low for a smooth servicing quality.

### Model
- Each message stream is represented using M<sub>i</sub> = (A<sub>i</sub>, maxD<sub>i</sub>)

### Comparison
- Algorithms
  - Dynamic approach v.s. Greedy approach
- Metrics
  - algorithm computational time
  - accept ratio of messages
  - scheduling jitter
  
### To Check
- When assign a new message, did the author consider the impact of assignment on future arriving messages?
