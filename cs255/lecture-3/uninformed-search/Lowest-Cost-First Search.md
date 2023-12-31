### Use Case
When we want to search a structure where edges have associated costs
### Methodology
- The cost of the path is the sum of the costs of its constituent edges
- An **optimal solution** is a path to a goal state with minimum cost
- The main structure is a min priority queue ordered by path cost
#### Notes
- Due to the last point, the first solution discovered will be optimal
- When all edge costs are equal, this is equal to [[BFS Graph Search]]