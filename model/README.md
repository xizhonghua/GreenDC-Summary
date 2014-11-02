## Model


### Migration
- Immediate dispatch, `My comment: it seems non-migration`
    - An online scheduling algorithm has the immediate dispatch property if it assigns a job J<sub>i</sub> to a server at time r<sub>i</sub>, and all jobs are processed exclusively on the server that they are assigned.
    - Immediate dispatch might be desirable for example if you had a load balancer sitting in front of a server farm, and migrations of jobs between servers was undesirable. 
    
### Measurement
- l<sub>p</sub> norms of flow and stretch
    - Often server systems do not implement the best known algorithms for optimizing average Qualify of Service(QoS) out of concern that these algorithms may be insufficiently **fair** to individual jobs.
    - One standard way to compromise between optimizing for the average and optimizing for the worst-case is to optimize the l<sub>p</sub> norm, generally for something like p =2 or p=3
    - Example
        - The standard way to fit a line to collection of points is to pick the line with minimum least squares, equivalently l<sub>2</sub>, distance to the points. And Knuth''s TexTypesetting system uses l<sub>3</sub> metric to determine line breaks.
    - The l<sub>p</sub>, 1 < p <&infty;, metric still considers the average in the sense that it takes into account all values, but x^p is strictly a convex function of x, the l<sub>p</sub> norm more severely penalizes outliers than the standard l<sub>1</sub> norm.