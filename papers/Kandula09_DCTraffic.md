## [The Nature of Datacenter Traffic: Measurements & Analysis](http://dl.acm.org/citation.cfm?id=1644918)

- status: started on 12/14/2014
- bib
```
@inproceedings{Kandula:2009:NDC:1644893.1644918,
 author = {Kandula, Srikanth and Sengupta, Sudipta and Greenberg, Albert and Patel, Parveen and Chaiken, Ronnie},
 title = {The Nature of Data Center Traffic: Measurements \& Analysis},
 booktitle = {Proceedings of the 9th ACM SIGCOMM Conference on Internet Measurement Conference},
 year = {2009},
 pages = {202--208},
 numpages = {7}
} 
```

### Summary


### Workloads Characteristics
- Traffic InterArrival: busty, long-tail
```
If flow arrivals were a
Poisson process, network designers could safely design for the average
case. Yet, we see evidence of periodic short-term bursts and long
tails. The inter-arrivals at both servers and top-of-rack switches have
pronounced periodic modes spaced apart by roughly 15 ms. We believe
that this is likely due to the stop-and-go behavior of the application
that rate-limits the creation of new flows. The tail for these
two distributions is quite long as well, servers may see flows spaced
apart by up to 10s.
```
