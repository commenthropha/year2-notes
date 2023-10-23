## The Problem
### Input
Two arrays of *n* size where each array represents a ranking of songs
- My array of rankings: 1,2, ..., n
- Your array of rankings: a_1, a_2, ..., a_n
### Output
The number of **inversions** in the array
- Songs i and j inverted if i < j, but a_i > a_j
## Designing a Solution
1. **Divide:** Separate the list into two pieces *O(1)*
2. **Conquer:** Recursively count inversions in each half *2T(n/2)*
3. **Combine:** Count inversions where ai and aj are in different halves, and return sum of three quantities *O(n)*
### Combining Efficiently
![[Pasted image 20231021120633.png]]
## Analysis
### Recurrence Relation
Set *T(n)* = number of comparisons to merge sort an input of size *n*

We can work out the merge sort recurrence to define *T(n)*
- *T(n)* = 0 if *n* = 1 (a single element list is already sorted)
- *T(n)* ≤ *T(⌈n/2⌉)* + *T (⌊n/2⌋)* + *n* otherwise
	- Count inversions in left half
	- Count inversions in right half
	- Merge together
### Solution
Solution to the counting inversions recurrence is *T(n)* = *O(n log_2 n)*
## Implementation
![[Pasted image 20231021115804.png]]