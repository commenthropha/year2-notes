### Methodology
The idea behind Quiescent Search is to apply the evaluation function until we reach [[Quiescent Positions (Quiescent Search) |quiescent positions]]
- Non-quiescent positions are expanded until quiescent positions are reached
### Problems
Quiescent Search is vulnerable to the [[Horizon Problem|horizon problem]], thus making the following mistakes: 
-  Bad ‘stalling’ moves in the face of an inevitable reduction in utility
- Picking moves which appear good but soon turn bad (beyond the horizon)

Two techniques for avoiding the horizon problem are:
- [[Singular Extensions]]
- [[Forward Pruning]]