## The Problem
### Input
An *m* x *n* multi-dimensional array representing *m* vectors in the space R^*n*
### Output
A pair of *n* dimensional vectors with the smallest euclidean distance between them
## Designing a Solution
1. **Divide**: Draw vertical line L so that roughly ½n points on each side
2. **Conquer:** Find closest pair in each side recursively
3. **Combine:** Find closest pair with one point in each side
### Combining Efficiently
Let δ = min(euclidean distance LHS, euclidean distance RHS)
![[Pasted image 20231021123121.png]]
Find closest pair with a point in each side, assuming distance < δ
- Only need to consider points within δ of line L
- Sort points in 2δ-strip by their y coordinate
- Only check distances of those within those positions
### Proof
![[Pasted image 20231021123216.png]]
## Analysis
### Recurrence Relation
We can work out the closest pair recurrence to define *T(n)*
- *T(n)* = O(1) if *n* = 1 (a single element)
- T(n) = 2T(n/2) + O(n log n) otherwise
### Solution
We can solve the recurrence relation by recursion tree or telescoping to get T(n) = *O(n log^2 n)*

We can achieve O(n log n) with a more involved solution to the problem
- Don't sort points in strip from scratch each time
- Each recursive call returns two lists: 
	- All points sorted by y coordinate (for the strip)
	- All points sorted by x coordinate (for the line L)
- Get the new lists by merging the two pre-sorted lists
## Implementation
![[Pasted image 20231021123330.png]]