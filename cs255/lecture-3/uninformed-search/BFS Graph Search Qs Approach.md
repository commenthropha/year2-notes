Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- A frontier queue, ordered by the next path to be expanded
-  Closed Set
	- This contains the nodes that have been expanded
		- At each stage, if we need to expand a node in the closed set, then we ignore it and add that path to the 'pruned' column
- Pruned
	- This contains the paths that have been pruned
	- This column may be omitted if we have not been asked to prune multiple paths

| Step | Frontier Queue       | Closed Set  | Pruned |
| ---- | ----------- | ----- | ----- |
| 1    | A           |     | |
| 2    | <A,C> <A,E> <A,B> | A | |
| 3    | <A,E> <A,C,D> <A,B>| A, C |    |

The last remaining path after expanding all other ones is the correct one for the respective search technique

At each step:
- Expand the path at the head of the frontier queue in the previous step
- If the node to expand is not in the closed set:
	- Add new paths to the queue
	- Add the newly expanded node to the closed set
- Otherwise:
	- Add the path to the 'pruned' column