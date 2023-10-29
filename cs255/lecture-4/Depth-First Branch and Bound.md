### Use Case
We use the depth-first branch-and-bound algorithm in the case that there are multiple solutions and we only want the optimal solution
### Idea
Suppose that a solution with cost q has been discovered (using DFS)

If the search encounters a path p such that cost(p) + h(p) ≥ q, then p cannot be optimal (recall that h(p) is an underestimate), so it can be pruned

Hence in this way we can discard paths that don’t lead to an optimal solution, and each time we discover a new solution p", its cost is at most q so we replace our bound q with cost(p" ) and continue

When the search is complete, the most recently discovered solution is guaranteed to be optimal
#### Initial value of bounds?
∞
### Combining with other Techniques
- Branch-and-Bound can be combined with **[[Iterative-Deepening Search|iterative deepening]]** to explore a large search space
	- It can also be combined with **[[Cycle Pruning|cycle pruning]]** for the same effect
- Branch-and-Bound is never used alongside [[Multiple-Path Pruning|multiple-path pruning]] 
	- This is because it would eliminates our linear time complexity since we would need to store paths