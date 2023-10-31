 Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- A stack
- Node currently being expanded

A list should also be maintained to keep track of the expanded nodes

| Step | Stack       | Expanded Node  |
| ---- | ----------- | ----- |
| 1    | A           |     |
| 2    | C E B | A |
| 3    | E D B | C     |

Expanded: A, C, E...

At each step:
- Expand the node at the tail of the stack (assuming you add to the tail) in the previous step
	- Add new nodes to the stack
	- Update the current expanded node