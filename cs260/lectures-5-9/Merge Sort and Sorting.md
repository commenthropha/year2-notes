## The Problem
### Input
An array of *n* elements in some arbitrary order
### Output
An array containing the same elements in ascending order
## Designing a Solution
1. **Divide**: Divide the array into two halves *O(1)*
2. **Conquer:** Recursively sort each half *2T(n/2)*
3. **Combine:** Merge two halves to make a sorted whole *O(n)*
### Combining Efficiently
- Perform only a linear number of comparisons
- Use a temporary array to build the merged output
## Analysis
### Recurrence Relation
Set *T(n)* = number of comparisons to merge sort an input of size *n*

We can work out the merge sort recurrence to define *T(n)*
- *T(n)* = 0 if *n* = 1 (a single element list is already sorted)
- *T(n)* ≤ *T(⌈n/2⌉)* + *T (⌊n/2⌋)* + *n* otherwise
	- Sort left half
	- Sort right half
	- Merge together
### Solution
Solution to the merge sort recurrence is *T(n)* = *O(n log_2 n)*
### Proof
- Initially we assume n is a power of 2 for simplicity
- Then ⌈n/2⌉ = ⌊n/2⌋ = n/2
#### Proof by Recursion Tree
![[Pasted image 20231021114136.png]]
#### Proof by Telescoping
![[Pasted image 20231021114156.png]]
#### Proof by Induction
![[Pasted image 20231021114213.png]]