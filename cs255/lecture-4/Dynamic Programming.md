In short, this idea involves building a table of dist(n),  the actual distance of the shortest path from node n to a goal, for static graphs

This can be built backwards from the goal:
![[Pasted image 20231021155439.png]]

We can then use this locally to determine what to do at each step, defining a *policy* of which arc to take from a given node

There are is two main problems with this approach:
- Dynamic programming requires enough space to store the whole graph
- The dist() function needs to be recomputed for each goal