MCTS works to estimate the value of a node from the average utility over simulations of complete games (known as *playouts*) starting from the state.

A *playout policy* is used to determine which moves to determine during the playout:
- Some games can learn from self-play using neural networks
- Some games use game-specific heuristics
	- e.g. capture moves in chess
### Pure Monte-Carlo Tree Search
#### Methodology
A pure MCTS approach would be to:
- Do n simulations starting from the current state
- Track which moves from the current position have the highest win percentage
- This converges to *optimal play* as n increases
#### Considerations
It's often too expensive to perform such a large number of simulations, so we need to be *selective* about which parts of the search tree to explore.

This is driven by a *selection policy* which balances:
- Exploration of states which have had few playouts
- Exploitation of states having done well in past playouts to increase the accuracy of our estimate
### Methodology
Combining elements of pure MCTS and utilising selection policies, MCTS works by:
1. [[Selection (MCTS)|Selection]]
2. [[Expansion (MCTS)|Expansion]]
3. [[Simulation (MCTS)|Simulation]]
4. [[Back-Propagation (MCTS)|Back-Propagation]]

The above steps are repeated for a fixed number of iterations or until out of time, at which point the move with the highest number of playouts is returned
### Example
![[Pasted image 20231105132244.png]]
### Upper confidence bounds applied to trees (UCT)
UCT is an effective selection policy, based on an upper confidence bound formula:
![[Pasted image 20231105132411.png]]
U(v) = The total utility of playouts through v
N(v) = The number of playouts through v
C = A constant which balances exploitation and exploration

The time to compute a playout is linear in the depth of tree since only one move taken at each node
