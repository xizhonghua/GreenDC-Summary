## [Joint Scheduling of Tasks and Messages for Energy Minimization in Interference-aware Real-time Sensor Networks](http://www.computer.org/csdl/trans/tm/preprint/06547140.pdf)


### Summary
<!--
- What is the problem that is addressed in the paper? 
- Which techniques are used to prove the results or obtain the performance evaluation? 
- What are the main results/findings? 
Please do not copy sentences from the paper (or abstract), use your own words to show your own preparation/understanding.
-->
- In this paper, the author studies the problem of joint scheduling of tasks and messages for energy minimization in interference-aware manner for wireless sensor network(WSN). 
- They model the problem as a Mixed Integer Linear Programming(MILP) and design Dynamic Voltage Scaling(DVS) for tasks and Dynamic Modulation Scaling(DMS) for messages. 
- In addition, they design efficient slcak allocation for dense WSN

### Merits/Contributions
<!--In this part, try to identify the strong points of the paper. 
- How does it contribute to the field? 
- Is there anything particularly attractive about the approach (e.g. strong analytical results or comprehensive experimental evaluation)? 
- Any commendable aspects about the methodology?-->
- As claimed by the author, this paper studies a new problem that has not been studied in the field of scheduling in inference network with the obkective to minimize energy consumption. Previous works only study tasks or messages and didn't consider joint scheduling of these two aspects. Thus one of the contributions is their identify of such unstudies problem.
- To study this untrackable problem, they decompose it into subproblems and try to plug in existing solutions for each subproblem. 

### Weaknesses
- What are the drawbacks of the approach adopted in the paper? 
- Any flaws in the technical content? 
- Problems with the simulation methodology? 
- Any exaggerated claims not supported by simulations or technical findings? 
- Are the comparisons made against other solutions proposed in the same area?

### Questions
- The authors mention that there are several models proposed for interfrence modeling, and they use the protocol model proposed in ref[19]. However the author fail to give any reasons or comments of why they stick with this model rather than others. 
- It is not clear about the motivation of the decomposing the problem in this manner, i.e., why the proprosed approach is decomposed in these three phases? It would be better for the author to give an overview of the decomposition of the problem in the beginning of Section 5 before introduce each subproblem.

### Extensions
- Any open and interesting research problems that you can identify after reading this paper? 
- Can you propose any extensions to this work? If so, how?
