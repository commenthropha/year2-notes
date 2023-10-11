# Agent Architecture and Hierarchical Control
## Agent Architecture
### Agent Systems
We can define an [[agent system]] and abstract an [[agent]] as comprising a [[body]] and a [[controller]]
### Agent Functions
If we let T be the set of time points, we can define the following:
- a [[Percept Trace]]
- a [[Command Trace]]
- a [[Transduction]]
- a [[Causal Transduction]]

We can then think of:
- a [[controller]] as an implementation of a [[Causal Transduction|causal transduction]] 
- an [[agent]]'s history as a sequence of past + present percepts as well as past commands
- a [[causal transduction]] specifies a function from an [[agent]]'s history at time t into its action at time t
### Belief States
An [[agent]] does not have access to its entire history, only its [[belief State]] which encapsulates the information about its past that it can use for current and future actions
## Controller Functions
At every point in time a [[controller]] has to decide on what the [[agent]] should do and what it should remember as a function of percepts and its memory
### Diagram
![[Pasted image 20231009105658.png]]
### Examples 
For discrete time, a controller implements:
- [[Belief State Function]]
- [[Command Function]]
## Hierarchical Control
Rather than implementing an agent as a repeated imperative process of, *perception*, *reasoning* and *action*, we can use a [[Hierarchical Control|hierarchy of controllers]]

In order to facilitate this model, we add a third percept function `higher_percept(memory, percept, command)` 
	This produces a higher-level percept for the next controller up in the hierarchy
## Types of Agents
With the above background we can identity 5 types of agents, in increasing generality:
1. [[Simple Reflex Agent]]
2. [[Reflex Agents with Memory]]
3. [[Goal-Based Agents]]
4. [[Utility-Based Agents]]
5. [[Learning Agents]]