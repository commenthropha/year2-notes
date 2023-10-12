# Greedy Algorithms
### Definition
(Kleinberg & Tardos) An algorithm that builds up a solution in small steps

In other words, a greedy algorithm attempts to find a *global optimum* through *iterative local optimisation*, using a [[greedy rule|heuristic]] at each stage
## Illustrative Problems
Here we explore 2 problems in which a greedy algorithm produces an optimal solution
### Interval Scheduling Problem
#### The Problem
##### Input
A set of intervals I = [n] such that s(i) and f(i) refer to the start and finish time of interval i respectively
##### Output
The largest subset S⊆I such that no two intervals are [[incompatible intervals|incompatible]]
#### Designing a Solution (using principles of GA)
##### Intuitive Ideas
There are many natural rules one may suggest for this problem. A few intuitive ones are:
1. [[Earliest Start Time First]]
2. [[Shortest First]]
3. [[Fewest Incompatibilities First]]
4. [[Earliest Finish Time First]]
##### Correct Solution
[[Earliest Finish Time First]] is the optimal solution. It also stands that it's quite a natural idea: 
- you ensure that your resource becomes free as soon as possible while still satisfying one request
- in this way we can maximise the time left to satisfy other requests.
#### Algorithm based on Optimal Solution
```
Sort jobs by finish times so that f1 <= f2 <= ... <= fn 

A <- Empty Set 
for j = 1 to n { 
	if (job j compatible with A) 
		A <- A union {j} 
} 
return A
```
##### Time Complexity
With an O(n · log(n)) algorithm for sorting (e.g. merge sort), it follows that the algorithm can be implemented in O(n · log(n)) time overall
###### Note
You can prove optimality for the earliest-finish-first greedy algorithm using proof by contradiction.

More intricate details of this proof are available in the slides located at [https://moodle.warwick.ac.uk/mod/resource/view.php?id=2277492]



### Interval Colouring/Partitioning Problem
#### Scenario
Suppose that each request corresponds to a lecture that needs to be scheduled in a classroom for a particular interval of time. We wish to satisfy all these requests, using as few classrooms as possible. The classrooms at our disposal are thus the multiple resources, and the basic constraint is that any two lectures that overlap in time must be scheduled in different classrooms.
#### The Problem
##### Input
A set of intervals I = [n] such that s(i) and f(i) refer to the start and finish time of interval i respectively
##### Output
A coloring k : [n] → [d] where d is minimal and no two i, j where k(i) = k(j) are incompatible.
#### Designing a Solution (using principles of GA)
Recall the [[Earliest Start Time First]] rule proposed for the interval scheduling problem. While erroneous in that case, it is both correct and optimal for the interval colouring/partitioning problem.
#### Algorithm based on Optimal Solution
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
##### Time Complexity
With an O(n · log(n)) algorithm for sorting (e.g. merge sort), it follows that the algorithm can be implemented in O(n · log(n)) time overall
##### Proving Optimality
Given a set of intervals I = [n], let the depth of I be defined as the maximum number of mutually incompatible intervals

We claim the following:  the number of resources needed to colour I is at least the depth of I
###### Proof
- Suppose for contradiction that the claim is false
- Then I has a colouring k which uses d colours, where d is less than the depth of I
- Let S be a set of mutually incompatible intervals of size equal to the depth of I
- By the pigeonhole principle, at least two distinct elements of S share a colour w.r.t. k, which is a contradiction

 Therefore, the Earliest-Start-Time-First greedy rule is optimal for the Interval Coloring problem

## The Exchange Argument
