A method for solving a CSP
### General Idea
Preprocess our [[Constraint Network|constraint network graph]] and make it
	1. [[Domain Consistency|Domain Consistent]] (for unary constraints)
	2. [[Arc Consistency]] (for higher order constraints)

then eliminate the variables one-by-one and propagate the effect of that on the rest of the constraint network by passing the removed variables' constraints to their neighbours
### Algorithm
- If there is only one variable, return the intersection of the (unary) constraints that contain it
- Otherwise, select a variable X
- Join the constraints in which X appears, forming constraint R1
- Project R1 onto its variables other than X, forming R2
- Replace all of the constraint in which X appears by R2
- Recursively solved the simplified problem, forming R3 (etc.)
- Return R1 joined with Rn

When there is a single variable remaining, if it has no values, the network was inconsistent
### Example
![[Pasted image 20231031150030.png]]![[Pasted image 20231031150038.png]]
![[Pasted image 20231031150055.png]]
![[Pasted image 20231031150115.png]]
![[Pasted image 20231031150128.png]]