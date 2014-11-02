## [Competitive online scheduling for server systems](http://dl.acm.org/citation.cfm?id=1243411)

- reading status: ing 11/1/2014
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
 
 
### Technique
- [**Competitive ratio**](../algorithms/file/Competitiveness.md)

- **Local Competitive Argument**: one way to prove competitive ratio
    - Procedure
        - Let A(t) be the increase of the QoS measure for algorithm A at time t for some understood input I
            - e.g., If QoS measure was average response time, then A(t) is the number of jobs released but unfinished at time t
            - e.g., If QoS measure was average slowdown, then A(t) is the number of jobs released but unfinished by A at time t divided by the aggregate workload of these jobs. `My comment: not very clear`
        - An algorithm A is locally c-competitive if for all inputs I, and all time t, it is the case that A(t) &le; c*Opt(t)
            - Example: SRPT is optimal for average response 
                - Shortest Remaining Processing Time(SRPT)
                - one needs to show that at all times, SPRT always has the least possible number of unfinished jobs
            - Example: SRPT is 2-competitive for average slowdown
                - one needs to show that at all times t, SPRT is at most twice optimal with respect to the objective of minimizing the number of unfinished jobs at time t divided by the work of these jobs

- [Resource Augmentation](../algorithms/file/resourceAug.md)

### Clairvoyant online algorithm
- Definition: It requires knowledge of the jobs
    - e.g., Clairvoyant: SPRT requires knowledge of the work of the jobs 
    - e.g., NonClairvoyant: Shortest Elapsed Time First(SETF) runs the jobs that runs the least so far.


### Shortest Elapsed Time First(SETF)
- The competitive ratio of SETF in the number of jobs
    - 
