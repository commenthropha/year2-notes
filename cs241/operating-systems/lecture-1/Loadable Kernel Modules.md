- The most modern approach to OS design, common in implementations of UNIX and Windows
- Kernel provides essential core services; additional modules are dynamically loaded as the kernel is running
	- These modules may, for example, offer hardware drivers or implement file system access
### Advantages & Disadvantages
- Each additional module is able to directly communicate with any other
- This allows for the extensibility of a [[Microkernels|microkernel]] approach without the additional overhead