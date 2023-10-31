We can characterise a CSP as a graph search problem in the following way:
- A node is an assignment of values to some of the variables
- Neighbours of that node are one more or one less variable consistent with the constraints`
- The start node is the empty assignment
- A goal node is a total assignment that satisfies the constraints

Note the difference between a [[Constraint Network|constraint network graph]] and the graph mentioned here

A [[Constraint Network|constraint network graph]] is a representation of the CSP as a problem whereas the graph mentioned here is a representation of the _process_ of searching for a satisfying assignment

It's framing the this task as graph search through the space of possible assignments
![[Pasted image 20231031125808.png]]
