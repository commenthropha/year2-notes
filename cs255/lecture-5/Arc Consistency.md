For constraints with a larger [[Scope of a Constraint|scope]], we can define the accompanying notion of *arc-consistency*

We can enforce arc consistency 
### Definition
![[Pasted image 20231029102929.png]]
### Possible Outcomes Once All Nodes Are Made Arc-Consistent
1. One domain is empty
   - No solution
2. Each domain constrains a single value
   - Unique solution
3. Some domains have more than one value
   - There may or may not be a solution

Points 2 and 3 may be contradictory, but they arise from a subtle observation: arc-consistency is a *local property*:
- It only checks that, for each value of a variable in the scope of a constraint, the other variables in the scope each some some value which satisfies the constraint
- There is no guarantee that these values that agree are the same in each constraint

For example, suppose we have variables {X, Y, Z}, each with domain 1, 2, and two constraints X = Y and X != Y 
- Each arc here is arc-consistent, but clearly this CSP has no solution
- However, when each domain has a single value, there must be global agreement since every constraint is satisfied precisely by the single value which remains for each variable

If some domains have more than one value after each node is made arc consistent, we can apply a divide-and-conquer technique called [[Domain Splitting|domain splitting]] to find a solution
