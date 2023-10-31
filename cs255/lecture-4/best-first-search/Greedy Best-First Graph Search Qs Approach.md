- Similar to [[Lowest-Cost-First Search]] and it's accompanying [[Lowest-Cost-First Graph Search Qs Approach|approach]] with the only major difference being that we consider the attached heuristic to each node instead of edge costs
	- The same logic applies, where the cost of the path is the sum of the costs of its constituent node (heuristics)

Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- A min priority **frontier queue**, ordered by the total heuristic cost of the path, initially only containing a path only housing the root node with cost 0
	- Each path should be labelled <N1, N2... NK>n where n is the total heuristic cost of the frontier
-  Closed Set
	- This contains the nodes that have been expanded
		- At each stage, if we need to expand a node in the closed set, then we ignore it and add that path to the 'pruned' column
- Pruned
	- This contains the paths that have been pruned
	- This column may be omitted if we have not been asked to prune multiple paths
	
| Step | Frontier               | Closed Set | Pruned |
| ---- | ---------------------- | ---------- | ------ |
| 1    | A                      |            |        |
| 2    | AC_2 AE_3 AB_5         | A          |        |
| 3    | AE_3 ACD_4 AB_5        | A C        |        |
| 4    | ACD_4 AB_5 AEF_5 AEB_6 | A C E      |        |

At each step:
- Expand the path at the head of the frontier queue in the previous step
- If the node to expand is not in the closed set:
	- Update the queue with all new paths and heuristic costs
	- Add the newly expanded node to the closed set
- Otherwise:
	- Add the path to the 'pruned' column

If we have been asked to check for cycles:
- We get rid of paths containing cycles in the same manner as multiple paths

An **optimal solution** will be the first path discovered to a goal state with minimum cost