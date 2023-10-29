# Application Layer (Part 1)

## Addressing Processes
While network devices are identified by [[IP Address|IP addresses]], processes on a given device can be uniquely identified using [[Port Number|port numbers]]
### Sockets
[[Sockets]] are used by processes to send/receive messages
## Transport Layer Services
Application processes use [[Transport Layer Services|transport layer services]]
## Developing Network Applications
- When developing a [[Network Application|network application]], it is generally necessary to create the client side as well as the server side
- Developing only one side of the program is enough for applications specified by standard protocols such as HTTP or SMTP
### Socket Programming
If we want to builds client/server applications that communicate using sockets, we can write a program that creates these sockets and read/writes to these sockets using system calls

There are two socket types to reflect the two transport layer services:
- [[TCP (Transmission Control Protocol)|TCP Sockets]] (connection-orientated sockets)
- [[UDP (User Datagram Protocol)|UDP Sockets]] (connectionless sockets)

