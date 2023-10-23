# Informed Search
## Definition
Informed search, unlike uninformed search, makes use of domain-specific knowledge; this knowledge is represented in the form of a [[Heuristic Function|heuristic function]]
## Techniques
- The most basic informed search technique is [[Best-First Search|best-first search]]
- An extremely popular technique is [[A* search]]
	- Due to the worst case time/complexity levels being fairly disadvantageous, it is important for us to consider ways to [[Improving A*|improve the algorithm]]
- A technique for static graphs is [[Dynamic Programming|dynamic programming]]
## Direction of Search
The definition of search is somewhat symmetric: we can go from the start node to the goal node, or vice versa

We can use this notion to begin thinking about ideas such as:
- [[Searching Based on Branching Factor]]
- [[Bidirectional Search]]
- [[Island Driven Search]]
## Bounded Techniques
There are a number of systematic search techniques that takes a bound (cost or depth). Namely:
- [[Bounded Depth-First Search]]
- [[Iterative-Deepening Search]]
- [[Depth-First Branch and Bound]]
