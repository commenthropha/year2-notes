A technique for invoking behaviour whereby processes interact by sending messages to each other
### Kernel Role
- [[Kernel]] provides a logical communication channel
- [[System calls]] to the kernel are used to pass messages between processes
	- This results in greater overhead compared to the [[shared memory|Shared Memory Model]] as the system depends on the kernel each time
### Advantages
- Unlike the [[Shared Memory|Shared Memory Model]], there are no memory conflicts/race conditions that you have to avoid
### Disadvantages
- Greater overhead compared to the [[shared memory|Shared Memory Model]] as the system relies on the kernel every time it wants to pass a message to another process
### Use Cases
- For passing smaller amounts of data as
	no memory conflicts/race conditions need to be avoided
- Distributed systems as
	it is more easily implemented

### Designing a Message Passing interface
At minimum a message passing interface should implement:
	`send` and `receieve` system calls

There are two broad schemes for this:
1. [[Direct Message Passing]]
2. [[Indirect Message Passing]] (Preferred)
#### Synchronisation
In terms of synchronisation in message passing, the system can be:
1. [[Blocking]]
2. [[Non-Blocking]]
##### Buffering
We can decide whether we want to utilise a blocking or a non-blocking system based on the capacity of the memory buffer. There are 3 cases to consider:
1. [[Zero Capacity]]
2. [[Bounded Capacity]]
3. [[Unbounded Capacity]] (Hypothetical)