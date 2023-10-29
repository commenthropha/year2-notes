### Definition
Sockets are APIs between the application and transport layers that allow processes to send/receive messages
### How They Work
- Whenever the sender has a message to send, it creates a socket and writes the message onto the socket with proper addressing information
	- The layers below and the internet is responsible for carrying the message to the receiving process
- The receiver has another socket into which the message is written
	- The receiving process simply reads the message from the socket