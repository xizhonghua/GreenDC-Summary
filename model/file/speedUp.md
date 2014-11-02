## Speed-up Function

### Definition
- &Gamma;(s) is the speed function when a job assigned s servers
  - &Gamma;(s) = s, then the job is *parallelizable*
  - &Gamma;(s) = c, c is constant, then the job is not *parallelizable*, it means devoting additional processing resources to constant jobs does not result in any fater processing of these jobs

### Characteristic
- In any real application, speed-up function is **sublinear** and **non-decreasing**
  - *sublinear*: if doubling the number of servers at most doubles the rate at which work is completed on the job
  - *non-decreasing*: 
