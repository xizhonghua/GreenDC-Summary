## Definition of Randomized Online Algorithms

### Definition
- Randomizedonline algorithm are compared against an **oblivious adversary** that must specify the input before the online algorithm begins.
  - If the adversary is allowed to change the future input in response to the random events internal to the scheduling algorithm, then generally randomization is not so helpful to the online algorithm.


### Example
[[Pruhs-2007]](../../papers/Pruhs07_competitive-online-scheduling.md)
- RMLF is &theta;(logn loglogn) against an adversary that at all times know the outcome of all the random events internal to RMLF up until that time. This accounts for the possibility of inouts where **future jobs may depend on the past schedule**.
- RMLF is &theta;(logn)-competitive against an **oblivious adversary**.
