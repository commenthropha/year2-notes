### Methodology
- Systematically explores the assignment space, D, by instantiating the variables one at a time
- Evaluates each constraint predicate as soon as all its variables are bound
- Any partial assignment that does not satisfy the constraint is pruned
	- This often translates to pruning many of the full assignments that are tested individually in the [[Generate-And-Test Algorithm]]
### Pseudocode
The algorithm can be implemented recursively as follows:
![[Pasted image 20231024114158.png]]

