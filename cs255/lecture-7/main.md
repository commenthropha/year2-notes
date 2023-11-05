# Adversarial Search
We can begin this section by defining the following:
- [[Games]]
- [[Adversarial Agents]]
### Introducing Minimax
The simplest type of [[Games|games]] consist of 2 players: a “maximising” [[Agent|agent]] Max and a “minimising” [[Agent|agent]] Min. 

We view the [[Utility Function|utility]] of the [[Games|game]] from the perspective of Max; a higher [[Utility Function|utility]] is better for Max and worse for Min, hence the names. 

Under the assumption that Min plays optimally, Max can exploit the structure of such [[Games|games]] to maximise their guaranteed [[Utility Function|utility]] using the **[[Minimax Algorithm]]**.
### Extending Minimax to α-β Pruning
While [[Minimax Algorithm|Minimax]] requires the whole search tree, this is often unnecessary – we can prune branches which will not influence our decision (because we already have a better choice). This is known as **[[Alpha-Beta Pruning]]**.