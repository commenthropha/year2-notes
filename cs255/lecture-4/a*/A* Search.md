### Methodology
- Unlike [[Best-First Search|best-first search]], A* uses [[Past Experiences|past information]] as well as present predictions to choose the best path
- A* treats the frontier as a **min-priority-queue** ordered by *f(x)* where:
	*f(x) = cost(x) + h(x)*
		*cost(x)* = cost from start to node p
		*h(x)* = estimate of cost to goal from p
### Complexity
#### Time Complexity
**Exponential** in (relative error of *h(x)*) * (length of solution *k*)
- In the worst case this becomes O(*b^k*)
	- This occurs when *h(x)* has a relative error of 1
#### Space Complexity
**Exponential** in the same way as time complexity
- This is because A* keeps all explored paths in memory
### Admissibility
We say that the algorithm is [[Admissible Algorithms|admissible]] if and only if
- The branching factor is finite
- Arc costs are bounded above zero
- *h(x)* is bounded above zero