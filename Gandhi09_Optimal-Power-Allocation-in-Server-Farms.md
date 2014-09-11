Optimal Power Allocation in Server Farms
---

- [PaperLink](http://www3.cs.stonybrook.edu/~anshul/sigmetrics_2009_tech.pdf)
- bib
```
@article{GaH09,
 author = {Gandhi, Anshul and Harchol-Balter, Mor and Das, Rajarshi and Lefurgy, Charles},
 title = {Optimal Power Allocation in Server Farms},
 journal = {SIGMETRICS Perform. Eval. Rev.},
 volume = {37},
 number = {1},
 month = jun,
 year = {2009},
 pages = {157--168},
 numpages = {12},
} 
```

### Background
- Server farms usually have a fixed peak power budget, since they are often billed by power suppliers based on their peak power requirement. The peak power budget of a server farm determines its cooling and power delivery infrastructure costs. Hence, companies are interested in maximizing the performance at a server farm given a fixed power budget.
- Power-to-frequency relationship.

### Summary
This paper investigates how to distributed available power among servers in a server farm so as to minimize mean response time, i.e., maximize performance.

### Extension
1. This paper only consider the response time. How about also taking into account the profits? i.e., make the objective as a mix function of response time and revenue.
