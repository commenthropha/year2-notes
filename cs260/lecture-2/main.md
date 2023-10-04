# Algorithm Analysis
### Motivations
We want to measure the **cost** of algorithms
- We use **running time** as the primary measure of cost
- Expressed as a function of some measure of the input size (n)
## Asymptotic Analysis
- Ignoring constant factors and lower order terms
- **Predicts** how the cost will grow as the input size increases
### Common types of Asymptotic Analysis
Two types of asymptotic analysis are:
1. [[Worst-Case Running Time]]
2. [[Average-Case Running Time|Average-Case Running Time]]

 A notable complexity for the runtime of an algorithm is [[Polynomial Time||polynomial time]].
### Notation
[[Big-O Notation]] is widely used for the purpose of algorithm analysis

We often say that T(n) = O(f(n)) which isn't very accurate.
- Instead, we should write T(n) ∈ O(f(n))
	- We should always aim to write our notation like this instead of using words which is ambiguous and verbose
#### Properties
Asymptotic notation satisfies transitivity rules
- If f = O(g) and g = O(h) then f = O(h)

Asymptotic notation follows additivity rules
- If f = O(h) and g = O(h) then f + g = O(h)
### Diagram
![[Pasted image 20231004141905.png]]