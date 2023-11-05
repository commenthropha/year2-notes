# Local Search
### Motivation
The search methods that we have explored so far are *systematic*; such methods apply poorly to [[Problems That Are Not Amenable To Systematic Search|some problems]] and we instead consider local search algorithms
### Definition
A *local search algorithm* is one which:
- Is not systematic
- Only maintains the current state (instead of multiple paths) and hence has low memory overhead
- Can find reasonably good solutions in large/continuous state spaces

Local search algorithms are part of a family of algorithms known as [[Iterative Improvement Algorithms|iterative improvement algorithms]]
#### Uses
Due to the properties of local search, it applies well to **optimisation problems** (e.g. softly-constrained CSPs) as well as discrete CSPs over large search spaces
#### State Space Visualisation
Let the state space be defined as *the set of complete configurations*, and the goal be defined as *a particular configuration (or set of configurations) that we are interested in*

Consider all states laid out on the surface of a landscape, where the height of any point represents the evaluation of the state at that point
![[Pasted image 20231031151200.png]]
We can then think about local search as moving around the landscape trying to find the highest peaks (or the lowest peaks if evaluation = cost and we would therefore want to minimise it)
## Techniques
- [[Hill-Climbing]]
- [[Local Search for CSPs (Greedy Descent)]]
- Parallel Search
- Beam Search

A similar, although not technically local search, notion is that of genetic algorithms 
