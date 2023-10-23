The relative error of heuristic directly affects the time complexity of A* 

This is because of the following property: 
- Suppose c is the actual cost of the shortest path from the start node to a goal node
- A* evaluates nodes in order of increasing *f(x)*, hence it evaluates all nodes with *f(x) < c* and some where *f(x) = c*
	- We never expand nodes where *f(x) > c* since we know *f(x)* must be an underestimate
- If *h(x)* is exact, then the size of first two sets is minimal, hence we expand the fewest nodes possible. 

To add to this, picking a heuristic that is cheap to compute will also reduce the time needed to perform A* (though it may not reduce asymptotic complexity). 

Hence we can say that a good heuristic is **[[Admissible Heuristic|admissible]], accurate and cheap to compute**