### Definition
- Mixture of one-to-one and many-to-one models
- Allows user-level threads to be multiplexed onto smaller or equal number of kernel level threads
### Diagram
![[Pasted image 20231105135549.png]]
### Advantages
- Kernel threads can run in parallel
	- Blocking a call from one user-level thread does not block the entire process
- Programmers can decide how many kernel threads to use and how many user level threads should be mapped to each one; this leads to less overhead