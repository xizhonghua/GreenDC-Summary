## [Joint Scheduling of Tasks and Messages for Energy Minimization in Interference-aware Real-time Sensor Networks](http://www.computer.org/csdl/trans/tm/preprint/06547140.pdf)

- reading status: finished on 10/22/2014
- note: paper summary for course CS773

### Summary
<!--
- What is the problem that is addressed in the paper? 
- Which techniques are used to prove the results or obtain the performance evaluation? 
- What are the main results/findings? 
Please do not copy sentences from the paper (or abstract), use your own words to show your own preparation/understanding.
-->
- In this paper, the author studies the problem of joint scheduling of tasks and messages for energy minimization in interference-aware manner for wireless sensor network(WSN). 
- They model the problem as a Mixed Integer Linear Programming(MILP) and design Dynamic Voltage Scaling(DVS) for tasks and Dynamic Modulation Scaling(DMS) for messages. 
- In addition, they design efficient slack allocation for dense WSN.

### Merits/Contributions
<!--In this part, try to identify the strong points of the paper. 
- How does it contribute to the field? 
- Is there anything particularly attractive about the approach (e.g. strong analytical results or comprehensive experimental evaluation)? 
- Any commendable aspects about the methodology?-->
- As claimed by the author, this paper studies a new problem that has not been studied in the field of scheduling in inference-aware wireless sensor network with the objective to minimize energy consumption. Previous works only study tasks or messages and didn't consider joint scheduling of these two aspects. Thus one of the contributions is their identification of such unstudied problem.
- To study this intractable problem, they decompose it into subproblems and try to plug in existing solutions for each subproblem. This is one of the good ways to study intractable problem.
- In the simulation, the performance is evaluated under various settings, i.e., various slack factor, various node number, various packet size and various inter-node distance, various cluster size, computation cycles. Also both the job makespan and energy consumption are evaluated. 

### Weaknesses & Questions
<!-- - What are the drawbacks of the approach adopted in the paper? 
- Any flaws in the technical content? 
- Problems with the simulation methodology? 
- Any exaggerated claims not supported by simulations or technical findings? 
- Are the comparisons made against other solutions proposed in the same area?-->
- In fig 11, it is not explained why the makespan has minimum value when the cluster size is 5. 
- The authors mention that there are several models proposed for interference modeling, and they use the protocol model proposed in ref[19]. However the author fail to give any reasons or comments of why they stick with this model rather than others. 
- It is not clear about the motivation of the decomposing the problem in this manner, i.e., why the proposed approach is decomposed in these three phases? It would be better for the author to give an overview of the decomposition of the problem in the beginning of Section 5 before introducing each subproblem.
- For the simulation, due to lack of research in this specific problem, the author compare their proposed approach with the theoretical upper bound generated by MILP, as well as with the other two weak versions of the developed algorithms. However, I am not very convinced of this design of experiments. It would be better for the authors to also compare with exiting approaches that work under similar settings with theirs, the setting may not need to be exactly the same. For example, maybe one only considers optimizing tasks scheduling, or maybe one only considers energy-aware message scheduling. It seems Ref[14] might be comparable which only considers DVS rather than consider both DVS and DMS. 



### Extensions
<!--- Any open and interesting research problems that you can identify after reading this paper? 
- Can you propose any extensions to this work? If so, how?-->
- Joint scheduling of tasks and messages with other objectives in interference-aware real-time sensor networks, such as average delay, worst-case delay etc. e.g., Ref[11] considers the joint scheduling with the objective to maximize the number of clients that can be scheduled with limited processor capacity and link capacity; in this paper, the authors consider joint scheduling with the objective to minimize power consumption.
- In this paper, the authors decompose the intractable problem into subproblems and then put efforts to solve each subproblems. Using same idea, maybe we can solve this problem with other decomposing manner, e.g., instead of decompose into three phases, maybe two phases or four phases. 
- As the author mentioned in Ref[19], there are several models proposed for interference modeling. The authors pick up the model in Ref[19]. Maybe we can study the same problem under the other models.