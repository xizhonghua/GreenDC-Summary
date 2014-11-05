## How to Analyze Competitive Ratio

### Method 1: Local Competitive Argument
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


### Method 2: Amortized Local Competitiveness
- Ref: [[Pruhs-2007]](../../papers/Pruhs07_competitive-online-scheduling.md)
- Exmaple
    - [[Edmonds-2000]](http://dl.acm.org/citation.cfm?id=301299) proves that Round Robin(RR) is (2+&epsilon;)-speed O(1)-competitive. 
- Motivation
    - Since a local competitiveness argument cannot work here, we need to develop a new technique: amortized local competitiveness. 
- Procedure
    - Let A be an arbitrary online scheduling algorithm.
    - Let A(t) be the *rate* of increase of the objective at time t
    - The algorithm A is *amortized locally c-competitive* with *potential function* &Phi;(t) if the following two conditions hold:
        - **Boundary**: &Phi; is initially 0, and finally nonnegative.
        - **Job Arrival**: &Phi; does not increase when a new job arrives.
        - **Completion**: &Phi; does not increase when either the online algorithm or the adversary complete a job.
        - **Running**: For all times t when no job arrives or is completed A(t) - c*Opt(y) + d&Phi;(t)/dt &le; 0 
    - By the above conditions, and integrating the above equations, we have
        - A(t) + \sum_(t<sub>i</sub>) &Delta;(&Phi;(t<sub>i</sub>)) &le; cOpt(I)
        - By the job arrival and the completition condition, we have A(I) + &Phi;(infinity) - &Phi;(0) &le; cOpt(I)
        - and finally by the boundary condition, we have A(I) &le; cOpt(I)
- Intuition
    - One can think of the potential function &Phi; as a bank. 
        - When A(t) &lt; cOpt(t), A is doing better than it needs to, and can save money in the bank
        - When A(t) &gt; cOpt(t), A is oding worse than it can afford to, and thus must withdraw money from the bank to pay for this
    - The condition above just imply that A cannot cheat the bank, for example, by not paying back money that it borrowed.

### Method 0: Amortized Analysis
- from Fei.
