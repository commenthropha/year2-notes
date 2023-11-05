### Formal Definition
An additional intuition for the [[Minimax Algorithm]] whereby we prune branches of the search tree that will not influence decision
### Methodology
Minimax is a depth-first search, and alpha-beta pruning gets it name from the parameters backed up the path
- α = value of best choice along the path for Max (highest value)
- β = value of best choice along the path for Min (lowest value)

Alpha-beta search updates α & β as it searches, pruning as soon as the value of the current node is known to be worse than current α or β for Max or Min respectively
- Pruning is done by terminating the recursive call
#### Example
![[Pasted image 20231105122242.png]]
### Effectiveness
The effectiveness of alpha-beta pruning depends on the order we examine successor states:
- If we could always examine the best successors first, Minimax with α-β pruning runs in time O(b^d/2)
	- This is compared to the O(b^d) time complexity offered by the base [[Minimax Algorithm]]
- If we examine successors in random order, the time complexity is increased to O(b^3d/4)
### Imperfect Decisions
Despite its efficiency improvements, Minimax with α–β pruning still needs to examine the search tree down to the terminal nodes
- Where a move (in a game) must be timely, this is not practical

An alternative is to cut off the search earlier using a heuristic evaluation function, which gives an estimate of the expected utility of a node, and a cutoff test to determine when to stop going down the tree

By cutting off the tree, we treat the internal nodes at the cutoff as terminals
- The cutoff can be: 
	- Set to a fixed depth d ∈ N
	- Dynamic adjusted with iterative deepening
- Both methods are unreliable due to the often approximate nature of the evaluation function

An alternative which deals with this issue is [[Quiscent Search]]