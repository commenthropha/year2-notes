Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- A queue
- Node currently being expanded

A list should also be maintained to keep track of the expanded nodes

| Step | Queue       | Expanded Node  |
| ---- | ----------- | ----- |
| 1    | A           |     |
| 2    | C E B | A |
| 3    | E D B | C     |

Expanded: A, C, E...

At each step:
- Expand the node at the head of the queue in the previous step
	- Add new nodes to the queue
	- Update the current expanded node