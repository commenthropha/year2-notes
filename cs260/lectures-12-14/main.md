# Dynamic Programming
### Definition
Breaking up a problem into a series of overlapping sub-problems and build up solutions to the whole
#### Conditions
- We require the 'optimal substructure' property: that the optimal solution can be built up from optimal solutions to subproblems
- We want that the number of subproblems does not grow too big
### Variations
Including accompanying illustrative problems
- [[One Dimensional Dynamic Programming (Weighted Intervals)]]
- [[Multiway Choice (Segmented Least Squares)]]
- [[Two Dimensional Dynamic Programming (Knapsack)]]
- [[Dynamic Programming for Sequences and Strings]]
- [[Reducing Memory Cost for Tables By Reusing Space]]
### Generic Approach
1. Characterise structure of problem
2. Recursively define value of optimal solution
3. Compute value of optimal solution efficiently
4. Construct optimal solution from computed information

There are several dynamic programming patterns to consider:
- Binary Choice ([[One Dimensional Dynamic Programming (Weighted Intervals)|Weighted Intervals]])
- Multiway Choice ([[Multiway Choice (Segmented Least Squares)|Segmented Least Squares]])
- Adding a new variable ([[Two Dimensional Dynamic Programming (Knapsack)|Knapsack]])

It is a personal preference whether to approach the problem top-down vs bottom-up
- The former builds a solution up incrementally while the latter is defined recursively