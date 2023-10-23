A technique for invoking behaviour whereby processes interact by reading from/writing to a shared region of memory
### Kernel Role
- [[Kernel]] is only involved in establishing the shared part of memory
	- Communication is handled entirely by the communicating processes
### Advantages
- As communication is handled entirely by the communicating processes, there is little overhead compared to [[message passing]]
	- This is because systems which use [[message passing]] are typically implemented using [[system calls]] which rely on kernel intervention
### Disadvantages
- Memory conflicts/race conditions can occur without the proper protection
### Different Types of Processes
In this model there are two types of processes:
- [[Producer processes]]
- [[Consumer processes]]
This is sometimes referred to as the [[Producer-Consumer Paradigm]]
#### How to prevent reading/writing when buffer is full/empty?
- Implement the buffer as a circular queue
	- Maintain pointers to the front and rear of the stored sequence of elements
		- Using modular arithmetic on the pointers, we can tell when the queue is
			 empty
				(when the pointers are at the same position)
			 full
				 (when the rear pointer is directly behind the front pointer)

