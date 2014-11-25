## Service Level Agreement

### Example
- [[Chen-2014]](../../papers/Chen14-IGCC-participate-in-grid.md) defines the SLA as (d, &eta;)
  - D<sub>j</sub> = T<sub>j</sub>/T<sub>j,min</sub>: where T<sub>j,min</sub> represents the time of running the job j without any power capping
  - The SLA means Probability{D<sub>j</sub> < d} < &eta;
  - In the simulation, they set the SLA as (2,95%), which means at least 95% jobs need to have a servicing time less than twice of the shortest processing time. Typically, data center operators require that 95% precentile of servicing time, d<sub>95</sub>, stays below a certain threshold [[Gandhi-2012]](http://dl.acm.org/citation.cfm?id=2410779).
