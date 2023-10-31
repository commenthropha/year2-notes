For constraints with a larger [[Scope of a Constraint|scope]] (more than one variable) we can define the accompanying notion of *arc-consistency*
### Definition
![[Pasted image 20231029102929.png]]
### Possible Outcomes Once All Nodes Are Made Arc-Consistent
1. One domain is empty 
   - No solution to the CSP
2. Each domain constrains a single value
   - Unique solution to the CSP 
3. Some domains have more than one value
   - There may or may not be a solution to the CSP

If some domains have more than one value after each node is made arc consistent, we can apply a divide-and-conquer technique called [[Domain Splitting|domain splitting]] to find a solution
### Example
AIFCA: Example 4.6
![[Pasted image 20231031131448.png]]
It's worth nothing that whenever you change the domain of a variable, you must recheck its arcs