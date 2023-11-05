### Parallel Search vs Local Search
- While the advantage of local search is its low memory overhead, often have more memory to use
- To make use of this, we can maintain some constant number c individuals instead of one
	- By 'individual' we mean a total assignment
### Methodology
- At each stage, we update one individual in the population
- Whenever an individual is a solution, it can be reported
- This acts similarly to c restarts while maintaining a single individual, but parallel search uses c times the minimum number of steps to reach the solution