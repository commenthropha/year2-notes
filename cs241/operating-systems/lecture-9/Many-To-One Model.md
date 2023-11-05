### Definition
All user level threads within a process are mapped to a single kernel thread
### Diagram
![[Pasted image 20231105135348.png]]
### Advantages
- Less overhead
- More flexibility in thread management (done by user level thread library)
### Disadvantages
- Multiple user-level threads cannot run in parallel
- One blocking user-level thread causes the whole process to block