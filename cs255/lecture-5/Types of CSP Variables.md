Variables in a CSP are one of two types:
### Discrete Variables
- May have *finite* domains : for *n* such variables of domain size *d*, our CSP has *d^n* possible assignments
- May have *infinite* domains, and hence cannot enumerate all possible assignments
	- Domains must then be expressed via equations
		- Systems of linear equations are solvable in polynomial time via linear programming
		- Non-linear equations are not solvable in polynomial time (as far as we know)
### Continuous Variables
- Solved similarly to discrete variables with infinite domains