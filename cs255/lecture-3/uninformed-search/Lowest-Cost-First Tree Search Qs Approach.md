Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- A min priority queue, ordered by the total cost of the nodes, initially only containing the root node
	- Each element should be labelled A_n where n is the total cost
- Node currently being expanded

A list should also be maintained to keep track of the expanded nodes

| Step | Queue       | Expanded Node  |
| ---- | ----------- | ----- |
| 1    | A           |     |
| 2    | C_2 E_3 B_5 | A |
| 3    | E_3 D_4 B_5 | C     |

Expanded: A, C, E...

At each step:
- Expand the node at the head of the queue in the previous step
	- Update the queue with all new nodes and costs
	- Update the current expanded node