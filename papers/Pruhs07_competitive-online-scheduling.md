## [Competitive online scheduling for server systems](http://dl.acm.org/citation.cfm?id=1243411)

- reading status: finished 11/2/2014
- bib
```
@ARTICLE{Pruhs07,
 AUTHOR = {Pruhs, Kirk},
 TITLE = {Competitive Online Scheduling for Server Systems},
 JOURNAL = {SIGMETRICS Performance Evaluation Review},
 VOLUME = {34},
 NUMBER = {4},
 YEAR = {2007},
 PAGES = {52--58},
 NUMPAGES = {7}
} 
```

### Summary
In this paper, the authors illustrate the competitive online scheduling research community's approach to online server scheduling problems. 
- They enumerate some of the results related to response and slowdown.
- They explain some of the standard techniques.

### Model
- Server
 - speed s
- Job J<sub>i</sub>
 - release time r<sub>i</sub>
 - work p<sub>i</sub>, thus processing time demand is p<sub>i</sub>/s
 - completition time C<sub>i</sub>
 - preemption is allowed
- Quality of Service(QoS) measures
 - response of a job is: F<sub>i</sub> = C<sub>i</sub> - r<sub>i</sub>
 - slowdown of a job is: S<sub>i</sub> = F<sub>i</sub>/p<sub>i</sub>
   - e.g., a job with slowdown 2 behaves as though it was served by a dedicated speed 1/2 server.
 - [l<sub>p</sub> norm of flow and stretch](../model/file/lpNorm.md)
 - [Weighted Response](../model/file/weightedResponse.md)
- [Immediate Dispatch](../model/file/immediateDispatch.md)
 
### Technique
- [Competitive ratio](../algorithms/file/Competitiveness.md)
  - [Speed Scaling](../model/file/speedScaling.md)
- [Resource Augmentation](../algorithms/file/resourceAug.md)

### Algorithm Types
- [Clairvoyant Online Algorithm](../algorithms/file/clairvoyant.md)
- [Randomized Online Algorithm](../algorithms/file/randomOnline.md)



