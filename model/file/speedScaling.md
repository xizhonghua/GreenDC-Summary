## Speed Scaling


### Intro
- In current CMOS based processors, the speed satisfies the well know cube-root-rule, that the speed is approximately the cube root of the power.
- Thus, the operating system is faced with a dual objective optimization problem as it both wants to conserve energy, and optimize some Qualify of Service(QoS) measure of the resulting schedule.

### Characteristic
- If there is an upper bound on energy used, then there is no O(1)-competitive online speed scaling poclity for total response.
  - Consider the situation when the first job arrives.
    - The scheduler has to allocate a constant fraction of the total energy to this job; otherwise the scheduler would not be O(1)-competitive in the case that no more jobs arrive.
    - However, if many more jobs arrive in the future, then the scheduler has wasted a constant fraction of its energy on only one job.
  - By iterating this process, one obtains a bound of &omega;(1) on the competitive ratio with respect to the total response.
- [local competitiveness](../../algorithms/file/competitiveAnalyze.md) is generally not achievable in speed scaling problmes because the adversary may spend essentially all of its energy in some small period of time, making it impossible for any online algorithm to be locally competitive at that time. Thus [amortized local analysis](../../algorithms/file/competitiveAnalyze.md) is the tool of choice.

### Competitive analysis 
- see [[Pruhs-2007]](../../papers/Pruhs07_competitive-online-scheduling.md), page 57
