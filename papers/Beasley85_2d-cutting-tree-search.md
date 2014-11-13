## [An Exact Two-Dimensional Non-Guillotine Cutting Tree Search Procedure](http://www.jstor.org/stable/170866)

- reading status: haven't started
- bib
```
 @article{Beasley85,
     title = {An Exact Two-Dimensional Non-Guillotine Cutting Tree Search Procedure},
     author = {Beasley, J. E.},
     journal = {Operations Research},
     volume = {33},
     number = {1},
     pages = {49-64},
     year = {1985}
    }
```

### Intro
- Guillotine cut
 - a cut rom one edge of the rectangle to the opposite edge, parallel to the two remaining edges.
 
### Summary
In this paper, the authors consider the two-dimensional cutting problem of cutting a number of rectangular pieces from a single large rectangle so a to maximize the value of the pieces cut. 
- They develop a **Largrangean** relaxization of a zero-one integer programming formulation of the problem and use it as a bound in a tree search procedure.
- *Subgradient* optimization is used to optimize the bound derived from the Lagrangean relaxzation.
