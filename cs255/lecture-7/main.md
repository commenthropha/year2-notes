# Adversarial Search
We can begin this section by defining the following:
- [[Games]]
- [[Adversarial Agents]]
### Minimax
The simplest type of [[Games|games]] consist of 2 players: a “maximising” [[Agent|agent]] Max and a “minimising” [[Agent|agent]] Min. 

We view the [[Utility Function|utility]] of the [[Games|game]] from the perspective of Max; a higher [[Utility Function|utility]] is better for Max and worse for Min, hence the names. 

Under the assumption that Min plays optimally, Max can exploit the structure of such [[Games|games]] to maximise their guaranteed [[Utility Function|utility]] using the **[[Minimax Algorithm]]**.
#### Extending Minimax to α-β Pruning
While [[Minimax Algorithm|Minimax]] requires the whole search tree, this is often unnecessary – we can prune branches which will not influence our decision (because we already have a better choice). This is known as **[[Alpha-Beta Pruning]]**.
#### Extending Minimax to Include Chance
Games involving probability include chance nodes (in the search tree), each outcome/child node of which is labelled with a probability summing to 1.
![[Pasted image 20231105130617.png]]

In terms of evaluating [[Utility Function|utility]], we can interpret chance actions by finding their expected value.

The definition for the minimax value would then become:
![[Pasted image 20231105130345.png]]

Since MinimaxWithChance considers all outcomes of chances nodes, the time complexity is can be upper bounded by O(b^d · n^d) where:
n =  the number of distinct outcomes
b = branching factor of the search tree
d = depth of the search tree

We can prune chance nodes without looking at their children if we place bounds on the utility function, as this allows us to compute bounds (albeit loose ones) for the average without looking at the children.
### Monte-Carlo Tree Search
Recall that [[Alpha-Beta Pruning]] is limited by:
- The branching factor (in practice a higher branching factor reduces the depth that can be searched)
- The difficulty of defining the evaluation function

We can address these limitations by utilising [[Monto-Carlo Tree Search]]
