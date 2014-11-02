## Definition of Competitive Ratio

### Definition
- **Competitive ratio**
    - Definition: *max A(I)/Opt(I) &le; c*, for any input instance I
        - A(I): the QoS measure of the schedule produced by algorithm A on input I
        - Opt(I) is the optimal QoS value
    - Explain: Since the competitive ratio is a worst-case concept, one generally thinks of the competitive ratio as the pay-off of a game played between the *online scheduling algorithm A* and the *adversary*
        - Algorithm A's move at time t is to specify the job that it will run
        - Adversary's move at time t is to specify the jobs that arrive at time t
        - The payoff of the game is then essentiallly the relative different between the QoS measurement of A's schedule and the QoS measure of the optimal schedule
