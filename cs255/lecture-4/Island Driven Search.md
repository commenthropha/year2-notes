This builds upon [[Bidirectional Search|bidirectional search]] and is the idea of identifying a set of m "islands" through which our path between start and goal passes
- There are now m smaller problems rather than 1 big problem
- We can then apply the same simultaneous search technique to lower the time complexity to mb^k/m ≪ b^k
- The problem is to identify the islands that the path must pass through, which may need problem-specific knowledge 
	- It is also difficult to guarantee optimality