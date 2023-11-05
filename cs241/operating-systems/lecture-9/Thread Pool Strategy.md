### Outline
- Server pushes new requests onto a common work queue
- Threads in a pool of fixed size pull and serve requests from this queue when idle
### Diagram
![[Pasted image 20231105140151.png]]
### Advantages
- Usually slightly faster to service a request with an existing thread than create a new thread
- Allows the number of threads in the application(s) to be bound to the size of the pool
	- The size of the pool is determined by the programmer taking into account the number of cores, memory in use, etc.
### Disadvantages
- A request may have to wait in a queue if all workers are busy
- Deciding the number of workers in the threadpool is not easy
	- May have to be adjusted dynamically depending on the load