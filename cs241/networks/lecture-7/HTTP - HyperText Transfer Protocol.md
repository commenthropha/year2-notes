### How it works
HTTP uses [[TCP (Transmission Control Protocol)|TCP]] as the transport layer protocol and port 80. At a high level, data is exchanged using HTTP via the following process:
1. The server starts on port 80
2. The client initiates a [[TCP (Transmission Control Protocol)|TCP]] connection to the server, on port 80
3. A [[TCP (Transmission Control Protocol)|TCP]] connection is established after a handshake
4. HTTP messages are exchanged
	- A HTTP message is either a [[HTTP Request|request]] or a [[HTTP Response|response]]
5. The [[TCP (Transmission Control Protocol)|TCP]] connection is closed
### HTTP Connection Types
There are two different methods of exchanging multiple objects over HTTP:
- [[Persistent HTTP Connection|Persistent]]
- [[Non-Persistent HTTP Connection|Non-Persistent]]
