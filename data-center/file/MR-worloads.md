## Map Reduce Workloads


- MapReduce Framework [[Jeff Dean-2004]](http://static.googleusercontent.com/media/research.google.com/en/us/archive/mapreduce-osdi04.pdf) and its Hadoop implementation [[Apache]](http://hadoop.apache.org/) 

### MapReduce
MapReduce is a framework for processing large data sets on server clsuters [[Jeff Dean-2004]](http://static.googleusercontent.com/media/research.google.com/en/us/archive/mapreduce-osdi04.pdf). 
- Each MapReduce program defines two functions: map and reduce.
  - Map
    - The framework divides the input data into a set of blocks, and runs a map tasks for each block that invokes the map function on each key/value pair in the block. 
    - The framework group together all intermediate values produced b the map tasks with the same intermediate key.
  - Reduce
    - It then runs the reduce tasks, each of which onvoles the reduce function of each intermediate key and its associated values form a distinct subset of generated intermediate keys. 
    - The reduce tasks generate the final result.
- TODO: get a MapReduce example

### Data-processing frameworks
- Characteristic: Bounded-delay
  - they are popular and often run many low-priority batch processing jobs, such as background log analysis, that **do not have strict completion time requirements**
  - they can be deplayed by a bounded amount of time
- Challenge
  - Scheduling the energy consumption of MapReduce jobs is challenging, because they do not specify the number of servers to use, their tun times, or their energy needs.
  - Moreover, power-mamanging servers in these frameworks requirs guranteeing that the data to be accessed by the jobs remain available.
  
