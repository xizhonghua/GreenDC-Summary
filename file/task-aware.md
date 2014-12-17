## Task-aware Scheduling


### Motivation
Many data center applications perform rich and complex tasks (e.g., executing a search query or generating a user's news-feed). From a network perspective, these tasks typically comprise multiple flows, which traverse different parts of the network at potentially different times. 
- Most network task resource allocation schemes, however, treat all these flows in isolation -- rather than as part of a task, and thereofore, only optimize flow-level metrics.

