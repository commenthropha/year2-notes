### Methodology
- Start with a depth bound b = 0 
- Do a bounded depth-first search with bound b 
- If a solution is found return that solution 
- Otherwise increment b and repeat
### Complexity and Analysis
- Iterative-deepening search finds the first same solution as breadth-first search
- Since it is using depth-first search, iterative-deepening uses linear space
- Iterative-deepening has an asymptotic overhead of (b/b-1) times the cost of expanding the nodes at depth k using breadth-first search
- When b=2 there is an overhead factor of 2, when b=3 there is an overhead of 1.5
	- As b gets higher (as in typical problems), the overhead factor reduces