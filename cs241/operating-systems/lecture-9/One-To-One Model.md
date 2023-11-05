### Definition
Each user-level thread maps to a kernel thread (e.g. Linux, Windows)
### Diagram
![[Pasted image 20231105135020.png]]
### Advantages
- Kernel is aware of all the threads running within the user process
	- Hence, the user process can completely rely on the kernel to manage (synchronise and schedule) its thread
### Disadvantages
- Creating each user-level thread involves the kernel; this is expensive
- User process is limited by thread management policies implemented by the OS