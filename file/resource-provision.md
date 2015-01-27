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
  
