## [Understanding Data Center Traffic Characteristics](http://dl.acm.org/citation.cfm?id=1672325)


- started on 12/12/2014, 
- bib
```
@article{Benson:2010:UDC:1672308.1672325,
   author = {Benson, Theophilus and Anand, Ashok and Akella, Aditya and Zhang, Ming},
   title = {Understanding Data Center Traffic Characteristics},
   journal = {SIGCOMM Comput. Commun. Rev.},
   volume = {40},
   number = {1},
   year = {2010},
   pages = {92--99},
   numpages = {8}
} 
```

### Summary
- how to traffic volumes and loss rates vary with time and with the location of a link in a multitier data center?
- What are the underlying arrival process and interarrival times that define data center traffic?
- How bursty is the traffic?


### Findings
- Average link loads
   - high in the core of data center switching architectures
   - fall progressively as one moves toward the edge
- Average link loss
   - higher at the edge
   - lowest at the core
- Packet arrival
   - data center edge can be characterized by ON-OFF pattern
   - packet interarrival times with an ON period follow **lognormal distribution**

