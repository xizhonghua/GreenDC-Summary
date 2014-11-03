## Prons and Cons for Competitive Analysis

- Ref: [[Pruhs-2007]](../../papers/Pruhs07_competitive-online-scheduling.md)

### Pros
- Scalability
  - It seems that for server systems, the key property of a good online scheduling algorithm is that it should scale as well as the optimal scheduling algorithm with the load.
    - Algorithms that are O(1)-competitive, or almost full scalable, have this scaling property.
  - This seems to be the reason that competitive analysis generally recommends the "right" algorithms
    - e.g., SRPT for average slowdown on a web server
    - e.g., SETF for average response on an operating system
    - e.g., LWT for average response on a multicase name server
- Requiring no probabilistic assumptions
  - One can reasonably obtain a competitive analysis for a wide varity of scheduling applications, without requiring probabilistic assumptions about the input distribution. 
    - it is often not clear what the "right" probabilistic assumption is, and if one assumes some general probability distribution, the resulting analysis is often intractable.


### Cons
- Since competitive analysis is a worst-case concept, the results are generally overly **pessimistic** for normal inputs.
- It only bounds the performance relative to the optimal algorithm, it does not give any absolute measure of the performance. So it might recommed a scheduling algorithm to run on your server farm, but it wouldn't tell you how many servers to buy to handle a certain number of users.
