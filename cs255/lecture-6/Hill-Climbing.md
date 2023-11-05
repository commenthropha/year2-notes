- Hill-climbing (or greedy local search) always tries to improve the state (or reduce cost if evaluation function is cost) 
- Each iteration, move in direction of increasing value (or decreasing if evaluation is cost - in which case the technique effectively becomes greedy descent) 
- There is no search tree, just keep current state and its cost 
- If several alternatives have equal value, choose one at random
### Algorithm
![[Pasted image 20231031155239.png]]
### Problems
- Local maxima (local peaks lower than highest peaks) cause the algorithm to halt with a sub optimal solution
- Plateauxs (flat areas)
	- If the plateaux is a local maxima, the search cannot progress
	- If the plateaux is a shoulder, we can progress by allowing sideway moves to try and get off of it
		- We must ensure that we limit the number of sideway moves, however, lest we risk conducting an infinite random walk on a plateaux
![[Pasted image 20231031155342.png]]
- Ridges with steep sides (and the top with a gentle slope) may cause the search to oscillate from side to side making no real progress
![[Pasted image 20231031155423.png]]