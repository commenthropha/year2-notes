### Formal Definition
In two-player games (where the players are Max and Min), Minimax gives the optimal strategy for Max assuming that Min plays optimally
### Minimax Value
The idea of the minimax algorithm is to choose the move with the highest minimax value at each point
#### Definition
The minimax value of a state is the [[Utility Function|utility]] (for Max) of being in that state assuming both players play optimally until the end of the game:
![[Pasted image 20231105115753.png]]
### Methodology
1. Generate the game tree
2. Label leaves/terminal nodes with their [[Utility Function|utility]]
3. Calculate the [[Utility Function|utility]] of the remaining nodes, working up the tree. For each node, keep track of the child which represents the best decision

Note: It is standard practice to label Max nodes with an upright triangle and Min nodes with an upside-down triangle
![[Pasted image 20231105115943.png]]
### Time Complexity
O(bd)
b = Branching Factor of search tree
d = Maximum Depth of search tree
### Space Complexity
O(b^d)
b = Branching Factor of search tree
d = Maximum Depth of search tree
### Completeness & Optimality
The minimax algorithm is:
- complete if the game tree is finite
- optimal if the opponent is also optimal