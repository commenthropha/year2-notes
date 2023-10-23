## The Problem
### Input
A set of intervals I = [n] such that s(i) and f(i) refer to the start and finish time of interval i respectively
### Output
The largest subset S⊆I such that no two intervals are [[incompatible intervals|incompatible]]
## Designing a Solution 
### Intuitive Ideas
There are many natural rules one may suggest for this problem. A few intuitive ones are:
1. [[Earliest Start Time First]]
2. [[Shortest First]]
3. [[Fewest Incompatibilities First]]
4. [[Earliest Finish Time First]]
### Correct Solution
[[Earliest Finish Time First]] is the optimal solution. It also stands that it's quite a natural idea: 
- you ensure that your resource becomes free as soon as possible while still satisfying one request
- in this way we can maximise the time left to satisfy other requests.
### Algorithm based on Optimal Solution
```
Sort jobs by finish times so that f1 <= f2 <= ... <= fn 

A <- Empty Set 
for j = 1 to n { 
	if (job j compatible with A) 
		A <- A union {j} 
} 
return A
```
### Time Complexity
With an O(n · log(n)) algorithm for sorting (e.g. merge sort), it follows that the algorithm can be implemented in O(n · log(n)) time overall
#### Note
You can prove optimality for the earliest-finish-first greedy algorithm using proof by contradiction.

More intricate details of this proof are available in the slides located at [https://moodle.warwick.ac.uk/mod/resource/view.php?id=2277492]