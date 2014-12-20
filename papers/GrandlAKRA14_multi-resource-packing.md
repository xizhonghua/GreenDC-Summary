## [Multi-Resource Packing for Cluster Schedulers](http://dl.acm.org/citation.cfm?id=2626334)

- started on 12/20/2014, end on
- bib
```
@inproceedings{Grandl:2014:MPC:2619239.2626334,
 author = {Grandl, Robert and Ananthanarayanan, Ganesh and Kandula, Srikanth and Rao, Sriram and Akella, Aditya},
 title = {Multi-resource Packing for Cluster Schedulers},
 booktitle = {Proceedings of the 2014 ACM Conference on SIGCOMM},
 year = {2014},
 pages = {455--466},
 numpages = {12}
} 
```

### Motivation
- Tasks in modern data-parallel clusters have high diverse resoruce requirements along CPU, memor, disk and network. 
- THus, a multi-resource cluster scheduler is needed, which will be responsible for packing tasks to machines based on their requirements of all resource types. With the following objective
 - avoids resource fragmentation
 - avoid over-allocation of the resources that are not explicitly allocated
