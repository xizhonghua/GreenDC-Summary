Internet Service
----

### Characteristic
The Internet services are supported by multiple data centers for high capacity, high availability, and low response time. The data center sit behind front-end devices that inspect each client request and forward it to one of the data centers according to a *request distribution policy*.

### Request Distribution Policy
These multiple data centers are capable of serving a collection of requests, i.e., they are mirrors with respect to the content requested, the service's front-ends can intelligently distribute the offered request load. Typically, a request can only be served by 2 or 3 mirrors. Further replicating content would increase state-coherence traffic without a commensurate benefit in availability or performance.

Current request-distribution policies over the wide area typically attempt to balance the load across mirror data centers, minimizing response time, and/or guarantee high availability.  For example, DNS attempts to balance the load by returning a different front-end for each DNS translation request. More interestingly. [Ranjan-2004](https://github.com/hxwang/Seminar/blob/master/Paper-Summary/RanjanK04_Wide-area-redirection-of-dynamic-content-by-Internet-data-centers.md) redirect dynamic-content requests away from an overloaded data center, if oding so is likely to produce a lower response time.
