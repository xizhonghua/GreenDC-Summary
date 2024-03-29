[A Linear Programming Approach to the Cutting-Stock Problem](http://www4.ncsu.edu/~kksivara/ma505/handouts/gilmore-gomory1.pdf)
---

- reading status: ing 11/09/2014
- bib
```
@article{GiG63
    author = {P.C. Gilmore, R.E. Gomory},
    title = {A Linear Programming Approach to the Cutting-Stock Problem},
    booktitle ={Operational Research},
    year = {1961}
}
```

### Intro
- When expressed as integer programming, the problem may be computation infeasible.
    - Reason: there could be large number of variables involved.
- How to overcome this problem?
    - Use the idea considered by [[Ford-1958]](http://dl.acm.org/citation.cfm?id=1245925) [[Dantzig-1960]](http://pubsonline.informs.org/doi/abs/10.1287/opre.8.1.101).
    - i.e., in the simplex method, when we reach the stage of "pricing out" or looking for a new column or activity that will improve the solution:
        - instead of looking over a vast existing collection of clumns to pick out a useful one, we simply create a column by solving an `anxiliary problem`.


### Problem Model
Given unlimited number of stocks with length L<sub>1</sub>, L<sub>2</sub>, ..., L<sub>k</sub>. There are incoming orders. An order consists of a request for a given number of N<sub>i</sub> of pieces of length l<sub>i</sub>.
- Different cuts could produce different set of l<sub>j</sub>, e.g., a cut could cut a stock of length 17 of three pieces, 5, 5, 4 , 3. Different cuts associate with different cost.
- The objective is to find the cutting approach that could minimize the cost as well as meet the demand of orders.

### My comments
- This problem model is different from cutting a rectangle to get a set of smaller rectangles.
