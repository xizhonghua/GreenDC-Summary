## Resource Provisioning

- Related research on resource provisioning
- Ref: [[Garg-2014]](http://www.buyya.com/papers/HeterogenousWorkloadCloud-ICA3PP2011.pdf)


### Virtualized Cloud Environment
- [[Meng-2010]](http://dl.acm.org/citation.cfm?id=1809052) proposed a joint-VM provisioning approach be exploiting *statistical multiplexing* among the workload patterns of multiple VMs, so that the unused resoruce of a low-utilized VM is borrowed by other co-located VMs with high utilization.
  - My comments: can be extend to combine heterogeneous workloads, renewable energy
- [[Steinder-2008]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4258530) takes advantage of virtualization features to co-allocated heterogeneous workloads on one server machine, thus reducing the granularity of resource allocation. 
  - My comments: this indicates that virtualization can increase system utilization!
- [[Eharqye-2010]](http://onlinelibrary.wiley.com/doi/10.1002/cpe.1468/pdf) developed a working prototype of a gramework for facilitating resource management in service providers, which allows both cost reduction and fulfill of the QoS based on SLAs. 
  - My comments: does this work consider mixed workloads?
- [[Quiroz-2014]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5353066) presented a decentralized and robust online clustering approach for a dynamic mix of heterogeneous applications on clouds, such as long running computationally intensive jobs, bursty and response-time sensitive requests, and data and IO-intensive analystics tasks. 
  - My comments: this work does not consider SLA penalties.
- [[Van-2009]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5328077) proposed a SLA-aware virtual resource management for cloud infrastructures, where an automatic resource manager controls the virtual environment which decouples the provisioning of resoruces from the dynamic placement of virtual machines. 
  - My comments: this paper considers SLA, but does not consider penalty. What is the approach used in this paper?
- [[Carrera-2008]](http://dl.acm.org/citation.cfm?id=1496964) developed a technique that enables existing middleware to fairly manage mixed workloads both in terms of batch jobs and transactional applications. The aim of this paper is towards a fairness goal while also trying to maximize individual workload performance.
  - My comments: for hetrogeneous workloads, the fairness is not very important as transactional workloads and batch jobs have different performance goals. 
- [[Hu-2009]](http://dl.acm.org/citation.cfm?id=1723041) developed an efficient and effective algorithm to determine the allocation stratgy that results in the smallest required number of servers.
- [[Nathuji-2010]](http://research.microsoft.com/pubs/118372/QClouds.pdf) proposed a QoS-awre control framework that tunes resource allocations to mitigate performance interference effects. These works only dealt with one type of application workloads and the number of applications is constant during resource application. 
  - While [[Garg-2014]](http://www.buyya.com/papers/HeterogenousWorkloadCloud-ICA3PP2011.pdf) dealty with multiple types of SLAs with admission control to allow more submisson of applications.
- [[Casalicchio-2013]](http://dl.acm.org/citation.cfm?id=2494623) proposed five resource allocation policies with workload prediction model to determine allocation or deallocation of new resources.
  - Comments: This work focuses on web-based applications not on batch type workloads.
- [[Zhu-2011]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6008764&tag=1) presented a datacenter architecture for hosting multi-tier web applictions using virtualized resources with an aim to satisfy users' SLA and maximize overall profit of IssA providers. 
- [[Qiu-2012]](http://link.springer.com/chapter/10.1007/978-3-642-29873-8_28#page-1) focusing on Online Transaction Processing systems, proposed an online algorithm for provisioning resources dynamically to minimize response time to end users. They utilize neural network based rechqniue to predict user demand on the system.
