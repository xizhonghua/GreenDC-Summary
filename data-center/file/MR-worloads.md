## Map Reduce Workloads

- Ref: [[Goiri-2012]](../../papers/GoiriL12_GreenHadoop.md)

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

### Hadoop 
Hadoop is the best-known, publicly available implmenetation of MapReduce [[Apache]](http://hadoop.apache.org/). Hardoop comprises two main parts.
- The Hadoop Distributed File System (HDFS) 
  - store data to be processed by a MapReduce program
  - it splits files across the servers' local disks
  - a cluster-wide namenode process maintains information about where to find each data block
- The Hadoop MapReduce framework
  
### Procedure
1. Users submit jobs to the framework using a client interface. 
  - This interface uses each job's configration parameters to split the input data and set the number of tasks.
  - Jobs must identify all input data at submission time.
2. The interface submit each job to the JobTracker, a cluster-wide process that manages job execution.
  - Each server runs a configurable number of map and reduce tasks concurrently in compute "slots"
  - The JobTracker communicates with the NameNode to determine the location of each job's data. It then selects servers to execute the jobs, preferably ones that store the needed data if they have slots available. Note, Haddoop's default scheduling policy is **FIFO**.




### Data-processing frameworks
- Characteristic: Bounded-delay
  - they are popular and often run many low-priority batch processing jobs, such as background log analysis, that **do not have strict completion time requirements**
  - they can be deplayed by a bounded amount of time
- Challenge
  - Scheduling the energy consumption of MapReduce jobs is challenging, because they do not specify the number of servers to use, their tun times, or their energy needs.
  - Moreover, power-mamanging servers in these frameworks requirs guranteeing that the data to be accessed by the jobs remain available.
  
