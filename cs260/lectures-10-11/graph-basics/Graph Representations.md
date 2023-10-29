### Adjacency Matrix
*n* x *n* matrix with A_uv = 1 if (u, v) is an edge
- Two representations of each edge
- Space proportional to n^2
- Checking if (u,v) is an edge takes Θ(1) time
- Identifying all edges takes Θ(n^2) time
#### Diagram
![[Pasted image 20231024132408.png]]
### Adjacency List
Node-indexed array of lists
- Two representations of each edge
- Space proportional to m+n
- Checking if (u,v) is an edge takes O(deg(u)) time
	- Recall that the degree of a node is the number of neighbours it has
- Identifying all edges takes Θ(m+n) time
#### Diagram
![[Pasted image 20231024133657.png]]