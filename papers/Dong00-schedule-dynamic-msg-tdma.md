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
