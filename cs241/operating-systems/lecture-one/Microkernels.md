- Only implement essential functionality
	- Includes memory management, CPU scheduling etc.
- Remove all non-essential components from the kernel and implement them as user-level programs
	- These communicate with each other using message passing
### Advantages
- Security and reliability -  operations with increased vulnerability are restricted to the kernel
- Extensibility - since new services are implemented at the user level, no work has to be done to modify the kernel
### Disadvantages
- Decreased performance due to increased system call overhead as user-level services must use [[message passing]] to communicate