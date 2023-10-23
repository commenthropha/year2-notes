A more complex source of wasted time is expanding nodes which take a non-optimal subpath between intermediate nodes where there are multiple possible subpaths.

We can prune multiple—paths by maintaining a closed list L of nodes at the end of paths that have been expanded. When a path {n0, ..., nk} is expanded: 
- Prune the path if nk ∈ L 
- Otherwise, keep the path and add nk to L 

If we simply remove the path in the first case, we may remove an optimal path. There are two ways to resolve this issue: 
- Remove all paths from the frontier which use the longer path 
	- i.e. if there is a path p = {s,... ,n,... ,m} on the frontier and a lower-cost path p' to n is found, then the p is removed from the frontier.
- Edit all such paths to use the new path
	- in the above example, we would replace the segment s...n in p with p'