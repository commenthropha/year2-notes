Given a connected graph G = (V, E) with real-valued edge weights Ce, a minimum spanning tree is a subset of the edges T⊆ E such that T is a [[Spanning Trees|spanning tree]] whose sum of edge weights is minimised
![[Pasted image 20231024155051.png]]
### Cayley's Formula
There are n^(n-2) spanning trees of K^n (the complete graph with n vertices)
- This means that brute force is not a feasible option
### Lemma 1
#### Claim
A [[cycles|cycle]] and a [[cutset]] intersect in an even number of edges
![[Pasted image 20231031092935.png]]
#### Proof
![[Pasted image 20231031092950.png]]
### MST via cut property
![[Pasted image 20231031093115.png]]
![[Pasted image 20231031093551.png]]
### MST via cycle property
![[Pasted image 20231031093142.png]]
![[Pasted image 20231031093600.png]]
## Algorithms to find MST
- [[Prim's Algorithm]]
- [[Kruskal's Algorithm]]