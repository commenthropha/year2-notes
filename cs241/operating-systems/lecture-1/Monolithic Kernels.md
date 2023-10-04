- Used by many early operating systems
- Typically did not have well-defined structures with all functionalities built into the kernel itself
### Advantages
- Little overhead in the system call interface
### Disadvantages
- Difficult to debug kernel code as little/no separation of concerns
- Early OSs didn't support dual mode operation
	- This created security vulnerabilities as sensitive memory/operations were accessible with fewer privileges