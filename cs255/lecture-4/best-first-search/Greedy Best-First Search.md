### Methodology
- Greedy Best-First search expends the path with the lowest heuristic value (i.e. the best path).
- Here we represent frontier paths with a **min-priority-queue** on the heuristic value, hence we can explore multiple paths at once 
	- We can think of this as exploring the *globally* best path
### Complexity
Since we store all explored paths, Greedy Best-First Search has **exponential** space overhead in the branching factor raised to the path length