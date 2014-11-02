## How to Analyze Competitive Ratio

### Method 1: Local Competitive Argument
one way to prove competitive ratio
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
