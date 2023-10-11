### Constituents
- A set of states S
	- With two subsets:
		1. Start states
		2. Goal states
- A set of possible actions which move us between states
- An action function which applies an action to a state, returning the new state:
	`state = update_state(action, state)`
- A criterion that specifies the quality of an acceptable solution
#### Representation
This information can take the form of a directed graph, where:
- S is the set of nodes 
- each edge (si, sj ) represents an action which moves the [[agent]] from state si to state sj