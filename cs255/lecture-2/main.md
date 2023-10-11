# Agent Architecture and Hierarchical Control
## Agent Systems
We can define an [[Agent System]] and abstract an [[Agent]] as comprising a [[Body]] and a [[Controller]]
### Agent Functions
If we let T be the set of time points, we can define the following:
- a [[Percept Trace]]
- a [[Command Trace]]
- a [[Transduction]]
- a [[Causal Transduction]]

We can then think of:
- a [[Controller]] as an implementation of a [[Causal Transduction|causal transduction]] 
- an [[Agent]]'s history as a sequence of past + present percepts as well as past commands
- a [[Causal Transduction]] specifies a function from an [[Agent]]'s history at time t into its action at time t
### Belief States
An [[Agent]] does not have access to its entire history, only its [[Belief State]] which encapsulates the information about its past that it can use for current and future actions
## Controller Functions
At every point in time a [[Controller]] has to decide on what the [[Agent]] should do and what it should remember as a function of percepts and its memory
### Diagram
![[Pasted image 20231009105658.png]]
### Examples 
For discrete time, a controller implements:
- [[Belief State Function]]
- [[Command Function]]