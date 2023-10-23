## Scenario
Suppose that each request corresponds to a lecture that needs to be scheduled in a classroom for a particular interval of time. We wish to satisfy all these requests, using as few classrooms as possible. The classrooms at our disposal are thus the multiple resources, and the basic constraint is that any two lectures that overlap in time must be scheduled in different classrooms.
## The Problem
### Input
A set of intervals I = [n] such that s(i) and f(i) refer to the start and finish time of interval i respectively
### Output
A coloring k : [n] → [d] where d is minimal and no two i, j where k(i) = k(j) are incompatible.
## Designing a Solution
Recall the [[Earliest Start Time First]] rule proposed for the interval scheduling problem. While erroneous in that case, it is both correct and optimal for the interval colouring/partitioning problem.
### Algorithm based on Optimal Solution
```
Sort the intervals by their start times, breaking ties arbitrarily 

Let I1, I2,..., In denote the intervals in this order 

For j = 1, 2, 3, . . . , n 
	
	For each interval Ii that precedes Ij in sorted order and overlaps it 
		Exclude the label of Ii from consideration for Ij 
	Endfor 
	
	If there is any label from {1, 2, . . . , d} that has not been excluded then 
		Assign a nonexcluded label to Ij 
	Else 
		Leave Ij unlabeled 
	Endif 
Endfor
```
### Time Complexity
With an O(n · log(n)) algorithm for sorting (e.g. merge sort), it follows that the algorithm can be implemented in O(n · log(n)) time overall
### Proving Optimality
Given a set of intervals I = [n], let the depth of I be defined as the maximum number of mutually incompatible intervals

We claim the following:  the number of resources needed to colour I is at least the depth of I
#### Proof
- Suppose for contradiction that the claim is false
- Then I has a colouring k which uses d colours, where d is less than the depth of I
- Let S be a set of mutually incompatible intervals of size equal to the depth of I
- By the pigeonhole principle, at least two distinct elements of S share a colour w.r.t. k, which is a contradiction

 Therefore, the Earliest-Start-Time-First greedy rule is optimal for the Interval Coloring problem