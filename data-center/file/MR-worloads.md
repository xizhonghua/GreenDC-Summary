## Map Reduce Workloads


- MapReduce Framework [[Jeff Dean-2004]](http://static.googleusercontent.com/media/research.google.com/en/us/archive/mapreduce-osdi04.pdf) and its Hadoop implementation [[Apache]](http://hadoop.apache.org/) 


### Data-processing frameworks
- Characteristic: Bounded-delay
  - they are popular and often run many low-priority batch processing jobs, such as background log analysis, that **do not have strict completion time requirements**
  - they can be deplayed by a bounded amount of time
- Challenge
  - Scheduling the energy consumption of MapReduce jobs is challenging, because they do not specify the number of servers to use, their tun times, or their energy needs.
  - Moreover, power-mamanging servers in these frameworks requirs guranteeing that the data to be accessed by the jobs remain available.
  
