# Divide and Conquer Algorithms
## Divide & Conquer
### Definition
(Kleinberg & Tardos) A class of algorithmic techniques in which one
1. **Divide:** Breaks the input into several parts
2. **Conquer:** Solves the problem in each part recursively
3. **Combine**: Merge the solutions to these sub-problems into an overall solution
### Analysing Running Time
Analysing the running time of a divide and conquer algorithm generally involves the use of a **recurrence relation**
### Applications
In many settings in which divide and conquer is applied, the natural brute-force algorithm may already be polynomial time, and the divide and conquer strategy serves to reduce the running time to a lower polynomial.
- This is different to the common case where brute force is usually exponential and the goal in designing a more sophisticated algorithm was to achieve **any** kind of polynomial running time
	- The overall theme of divide & conquer is that improving on brute-force search is a fundamental conceptual hurdle in solving a problem efficiently, and the design of sophisticated algorithms can achieve this
### Illustrative Problems
- [[Merge Sort and Sorting]]
- [[Counting Inversions]]
- [[Closest Pairs of Points]]
### Solving Recurrence Relations
[[The Master Method]] provides us with a quick way to solve common forms of recurrence relations that arise in this module
### Mathematical Applications
We can use divide and conquer algorithms to speed up fundamental mathematical operations. For example:
- Integer Multiplication
- Matrix Multiplication