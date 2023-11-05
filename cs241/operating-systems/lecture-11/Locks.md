### Definition
- A lock is a programming construct which can be held by only one process at a time
### Lock Management
- The acts of acquiring and releasing a lock are called *locking* and *unlocking* respectively
- These operations should be performed atomically (as a single, indivisible unit of work without interruption), otherwise you run into problems similar to that of [[Peterson's Algorithm|Peterson's algorithm]]
	- Modern machines provide *atomic hardware-level instructions* for this purpose
		- An example of this is the [[test_and_set]] instruction
	- Hardware-level instructions can be complicated and generally inaccessible to programmers
	- Instead, OS designers build [[Synchronisation Primitives|synchronisation primitives]] to allow programmers greater flexibility in solving [[The Critical Section Problem|the Critical Section Problem]]