Packing Algorithms
------


## 2D Packing
Allocate a set of rectangular items to large rectangular standardized units by minimizing the waste.
- 2D dimensional bin packing
 - these units are finite rectangles
- 2D dimensional strip packing
 - there is a single standardized unit of given width 
 - the objective is to pack all the items within the minimum height


 
### Problem Model
We are given a set of n rectangular items j \in J = {1,...,n}, each defined by a width, w<sub>j</sub>, and a height, h<sub>j</sub>.

- In the 2D bin packing problem (2BP)
 - We are further given an unlimited number of identical rectangular bins of width W and height H
 - The objective is to allocate all the items to the minimum number of bins
- In the 2D strip packing problem (2SP)
 - We are further given a bin of width W and **infinite height** (hereafter called strip)
 - The objectie is to allocate all the items to the strip by minimizing the height to which the strip is used.

### Assumption
- the items have to be packed with their w-edges **parallel** to the W-edge of the bins (or strips).


### NP hardness
- Both problems are strongly NP-hard, as is easily seen by transformation from the strongly NP-hard (one-dimentional) Bin Packing Problem (1BP)
- Reduce to 1BP
 - there are n items, each haveing an associated size h<sub>j</sub>, have to be partitioned into the minimum number of subsets so that the sum of the sizes in each subset does not exceed a given capacity H.
