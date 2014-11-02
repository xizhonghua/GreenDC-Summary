## Example of Competitive Ratio with Resource Augmentation

### Example
- SETF is (1+&epsilon;)-speed (1+1/&epsilon;)-competitive in terms of average response
  - This illustrates a phenomenon that is common in many scheduling problems: there is an almost fully scalable algorithm even though there are no O(1)-competitive algorithms
  - THe intition behind this is that if a system's load is near its cpacity, then the online scheduler has no time to **recover from even small mistakes**. 
  - Many of the strong worst-case lower bounds for online scheduling problems utilize input instance where the load is essentially the capacity of the system.
