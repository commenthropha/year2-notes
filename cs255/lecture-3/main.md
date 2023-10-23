# Problem Solving & Uninformed Search
## Problem Solving
A typical problem consists of a solution specification and a set of deterministic actions that an [[agent]] can take

A problem-solving agent takes the following steps:
1. [[Problem Formulation]]
2. [[Goal Formulation]]
3. [[Search]]
4. [[Execution]]

During the aforementioned steps, the agent may be:
- Offline
	- In this case, it doesn't acquire any new knowledge of the environment during the process
- Online
	- This is when the agent acts while gaining evolving knowledge about the environment

### Problem Solving as State-Spaces
We can represent problems as [[state-spaces]] to help us understand the problem better

In reality, the world is often too complex to represent all possible states and actions
	In these cases we make abstractions which allow for practical representations

### Problem Types
We can categorise problems as follows:
- [[Single State Problem|Deterministic, Fully Observable]] (Single State Problem)
- [[Multiple State Problem|Deterministic, Partially Observable]] (Multiple State Problem)
- [[Contingency Problem|Stochastic, Partially Observable]] (Contingency Problem)
- [[Online Exploration Problem|Unknown State Space, Knowledge is Learned]] (Online Exploration Problem)

## Uninformed Search 
Before we begin to look at search techniques, we introduce two important notions; that of:
- [[Admissible Algorithms]]
- [[Complete Algorithms]]
### Techniques
- [[Tree Search]]
- [[BFS Tree Search]]
- [[DFS Tree Search]]
- [[Graph Search]]
- [[BFS Graph Search]]
- [[DFS Graph Search]]
- [[Lowest-Cost-First Search]]