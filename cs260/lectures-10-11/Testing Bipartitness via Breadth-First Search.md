Many problems become:
- easier if the underlying graph is bipartite (matching)
- tractable if the underlying graph is bipartite (independent set)
### Lemma 1
#### Claim
If graph G is bipartite, it can't contain an odd length cycle
#### Proof
- Not possible to 2-colour an odd cycle, let alone G
- In fact, the absence of odd cycles characterises bipartiteness
### Lemma 2
#### Claim 
Let G be a [[Connectivity|connected graph]] and let {L0, ..., Lk} be the layers produced by Breadth-First Search starting at node *s*. Exactly one of the two cases holds:
1. No edge of G joins two nodes of the same layer and G is bipartite
2. Some edge of G joins two nodes of the same layer and G contains an odd-length cycle, hence G is *not* bipartite
#### Proof
##### Case 1
- {L0, ..., Lk} are the layers produced by Breadth-First Search of G starting at node *s*
- Suppose no edge joins two nodes in the same layer
- By the edge property of Breadth-First Search, all edges must instead join nodes on adjacent layers
- This leads us to a bipartition, therefore the original graph must also be bipartite
![[Pasted image 20231024151216.png]]
##### Case 2
![[Pasted image 20231024151456.png]]
### Corollary (continuing from Lemmas 1 and 2)
#### Claim
A graph G is bipartite **iff** it contains no odd length cycle
#### Proof
##### Proving Sufficiency (=>)
If G is bipartite, it has no odd length cycle via Lemma 1
##### Proving Necessity (<=)
If G has no odd length cycle then we are in the first case of lemma 2, so G is bipartite 
## Concluding Notes
To test for bipartiteness: 
- Run BFS and check for cross edges
	- If there are cross edges then G contains an odd length cycle and, thus, is not bipartite
![[Pasted image 20231024153456.png]]