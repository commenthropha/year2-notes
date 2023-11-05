We can apply local search to CSPs in the following way: 
- The current state is an assignment of variables
- A neighbouring state is one in which the value of one variable differs
- The goal is to find an assignment with no conflicts 
- The heuristic function to be minimised is the number of conflicts in our CSP

We have several possible strategies for selecting a variable and value to assign at each step:
- Find the variable-value pair which minimises the number of conflicts
- Select the value which minimises the number of conflicts for a variable which:
	- Participates in the most conflicts
	- Appears in any conflict
	- Is selected at random
- Select the variable and value at random
	- Accept if the assignment does not increase the number of conflicts
### Extended Ideas
- [[Complex Domains (Greedy Descent)|Complex Domains]]
- [[Randomised Greedy Descent]]
- [[Stochastic Local Search]]
