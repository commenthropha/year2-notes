### Methodology
- Heuristic DFS expands the node with the lowest heuristic value (i.e. the best node)
- As with [[DFS Graph Search]], nodes are stored as a stack, hence we explore all paths from an expanded node before exploring elsewhere
	- We can think of this as exploring the *locally* best path
### Complexity
Since we only store nodes along the current path, Heuristic DFS has **linear** space overhead in the length of the path