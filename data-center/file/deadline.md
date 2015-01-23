## Deadline

- ref [[Adnan]](../../papers/AdnanS12_dynamic-deferral-geoDC.md)


### Why associate job with deadline
- Many applications in real world require delay bound or deadline constraint [[Lee-2007]](http://dl.acm.org/citation.cfm?id=1272381). 
- A recent study on real-life production systems showed that there existed a long tail in processing delay for user requests; although accounting for less than 5% of the total, the user requests experiencing the longest delay significantly degraded users' experience [[Kavylya-2009]](http://dl.acm.org/citation.cfm?id=1845224) [[Ersoz-2007]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4268212). Thus it is necessary to provide a service delay bound to guarantee all user requests a completion deadline.

### Introduction of deadline-aware job scheduling
- When combine with energy conservation, deadline is usually a critical adjusting tool beween performance loss and energy consumption. 
- Energy efficient deadline scheduing was first studied by [[Yao-1995]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=492493&tag=1). They proposed algorithms, which aim to minimize energy consumption for independent jobs with deadline constraints on a single varianble-speed processor.


### Current research situation 
- In the context of greendata center, most work on energy management merely talk about minimizing the average delay but not give any bound on delay until recently. 
