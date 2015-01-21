## Heterogenous workload

### Background
- The operator of cloud service must schedule the stream of incoming applications on available servers in a manner that achieves both fast execution (users' goal) and high resource efficiency (operator's goal), enabling better scaling at low cost [[Delimitro-2013]](http://web.stanford.edu/~cdel/2013.asplos.paragon.pdf)
- This schedule is particularly difficult as cloud services must acommodate a diverse set of workloads in terms of resource and performance requirements [[Barroso-2009]](http://www.cs.berkeley.edu/~rxin/db-papers/WarehouseScaleComputing.pdf). 

### Why has heterogeneous workload
- With the increasing popularity of cloud computing, research centers and enterprises have started to outsourcing their IT and computational needs to on-demand cloud services [[Buyya]](http://www.sciencedirect.com/science/article/pii/S0167739X08001957). 


### Characteristic

### How current solutions deal with heterogenous workload
- Give higher priority to web server jobs. 
  - [[Zhan-2014]](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6205737): Web server requests require an immediate response, thus they have higher priority. While batch jobs can be queued when resource is not available.

### Evidence of heterogeneous workload
- Search engine systems, like Nutch(http://nutch.apache.org/), include two major heterogenous workloads: Map-Reduce like parallel data analysis and search engine services. [[Zhan-2014]](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6205737)
- The Boeing company also reported this trend of consolidating parallel batch jobs and web service applications on one data center in the recent IDC HPC user forum, held in October 30, 2010 at Beijing, China. [[Zhan-2014]](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6205737)
- Transactional applications and batch jobs are widely used by many organizations to deliver critical services to their customers and partners. For example, in financial institutions, transactional web workloads are used to trade stocks and query indices, while computationally intensive non-intensive workloads are used to analyse portfolios or model stock performance. [[Carrera-2008]](http://link.springer.com/chapter/10.1007%2F978-3-540-89856-6_11)
  - Past: Due to intrisic differences among these workloads, they are typically run today on separate dedicated hardware, which contributes to resource under-utilization and management complexity.
  - Future: Therefore, organizations demand management solutions that permit such workloads to run together on the same hardware, improving resource utilization while continuing to offer performance guarantees.
  

### Real-traces of heterogenous workload
