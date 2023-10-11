# Agent Architecture and Hierarchical Control
## Agent Systems
We can define an [[agent system]] and abstract an [[agent]] as comprising a [[body]] and a [[controller]]
### Agent Functions
If we let T be the set of time points, we can define the following:
- a [[percept trace]]
- a [[command trace]]
- a [[transduction]]
- a [[causal transduction]]

We can then think of:
- a [[controller]] as an implementation of a [[Causal Transduction|causal transduction]] 
- an [[agent]]'s history as a sequence of past + present percepts as well as past commands
- a [[causal transduction]] specifies a function from an [[agent]]'s history at time t into its action at time t
### Belief States
An [[agent]] does not have access to its entire history, only its [[belief state]] which encapsulates the information about its past that it can use for current and future actions
## Controller Functions
At every point in time a [[controller]] has to decide on what the [[agent]] should do and what it should remember as a function of percepts and its memory
### Diagram
![[Pasted image 20231009105658.png]]
### Examples 
For discrete time, a controller implements:
- [[belief state function]]
- [[command function]]
## Hierarchical Control