## Demand Response (DR) Event

- courtesy of [[Zois-2014]](../../papers/ZoisFCSP14-customer-selection-smart-grid.md) 

### Definition
A DR event is defined as a schedule consisting of customers and their corresponding strategies for a specific period of the day. It is initiated by energy providers to achieve a combined load reduction from the participating customers. 

### Sustainable Load Reduction
A DR event is said to be sustainable if it achieves consistent load reduction for the scheduled time frame. A consistent load reduction is considered to be a reductin of the typical powr consumption under a specified threshold. This threshold is usually defined by the utility providers. This threshod is usually defined by the utility providers. The goal can be to ensure reliability in power distribution, protect the equipment on the grid or simply maximize profit. 
- Sustainble load reduction is a hard problem.
  - Customers employed on top of the power grid are inherently unpredictable. This uncertainty hinders attempts on achieving sustainability.
  - Customer comfort [[Sepulveda-2010]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5697187&tag=1) is defined as the ability of users in the power grid to decide independently about the time and the way to consume power. Each one has a different footprint characterized by their behavior and different reactions to exogenous events (e.g., rise in temperature). When schedule a DR event, all of this has to be taken into consideration. It is imperative to deal with uncertainty, instead of replying too much o predictable loads in order to custain a consistent reduction. Hence it is important also to quickly (dynamic DR) react and adapt to changes induced by uncertainty from the behavior of individual customers. 
- If the above points are to be considered the sophisticated scheduling algorithm is needed. This algorithm should produce a selection of customers to participate in a DR event aming to minimize uncertainty while maximizing comfort.
