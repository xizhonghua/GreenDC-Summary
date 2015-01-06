## [Towards energy proportionality for large-scale latency-critical workloads](http://dl.acm.org/citation.cfm?id=2665718)

- reading status: start on 1/6/2015
- bib
```
@inproceedings{LoCGBK14,
 author = {Lo, David and Cheng, Liqun and Govindaraju, Rama and Barroso, Luiz Andr{\'e} and Kozyrakis, Christos},
 title = {Towards Energy Proportionality for Large-scale Latency-critical Workloads},
 booktitle = {Proceeding of the 41st Annual International Symposium on Computer Architecuture},
 series = {ISCA '14},
 year = {2014},
 pages = {301--312},
 numpages = {12}
} 
```

### Background
- **Energy proportionality**: Modern servers are not energy proportional, they operate at peak energy efficiency when there are fully utilized, but have much lower efficiencies at lower utilizations. 
 - While the average uilization of WSC systems for continuous batch workloads can be around 75%.
 - The average utilization of shared WSC systems that mix several types of workloads, including online services, maybe between 10% and 50% [[Luiz-2013]](http://www.morganclaypool.com/doi/abs/10.2200/S00516ED2V01Y201306CAC024).
 - **Observation**: At medium and low utilizations, the energy waste compared to an ideal, energy proportional system is significant. To improve the cost effectiveness of WSC systems, it is important to improve their energy efficient at low and moderate utilizations.
- Technical terms
 - OLDI: online, data-intensive
 - SLO: service level objectives

### Approach
- Scale the server's processing capacity to match the available work is a promissing way to improve energy efficienty for OLDI workloads at low or medium utilization.
 - We can reduce power consumption by scaling voltage and clock frequency (DVFS) or the number of active cores in the server.
 - Traditional DVFS schemes is controlled by monitoring CPU utilization.
 - However, they found OLDI workloads exihibit different latencies for the same CPU utilization at different CPU frequencies.
 - Thus, they proposed to manage the capacity of servers based on the observed, end-to-end, request latency.
