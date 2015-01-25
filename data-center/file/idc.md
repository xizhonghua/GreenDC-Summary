## Internet Data Center

- Ref: [[Lup-2013]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6566791)

### Model
- Front-end portal server, back-end distributed IDC system
  - A cloud-computing service provider usually operates a group of front-end portal servers and a back-end distributed IDC system. 
- **Portal Sever**
  - Each portal server aggregates user request originating from a service area. 
- **Distributed IDC system**
  - The distributed IDC system comprises a number of geographically separate IDC sites. 
- **Central Scheduler**
  - A central scheduler fulfills spatio-temporal load balancing, which decides the workload to dispatch from each portal server to distributed IDC systems. 

### Assumption
- Worloads
  - They assume that a user request can be decomposed to small user tasks; each user task can be executed on an IDC site in a time slot; tasks forming a user request may be forming a user request can be executed on multiple IDC sites in multiple time slots.
