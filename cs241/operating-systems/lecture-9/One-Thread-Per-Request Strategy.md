### Outline
Server creates a separate thread to handle each client request 
### Diagram
![[Pasted image 20231105135932.png]]
### Disadvantages
- High overhead for each thread
- High traffic will create a large number of threads, slowing down the system by burdening it
