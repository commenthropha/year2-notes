### Definition
A divide and conquer technique used to find a solution to a CSP if some domains have more than one value after all nodes are made arc consistent
### Methodology
This involves picking a variable, splitting its domain, and solving the CSP on each half of the domain; if either results in a solution then we have a solution for the original CSP

Note that domain splitting does require that we re-enforce arc-consistency for any arcs which may no longer be arc consistent as a result of the split
### Advantages
The time required to solve two smaller problems 2d^(n/2) is less than that of solving the problem outright d^n
### Example
![[Pasted image 20231031132025.png]]