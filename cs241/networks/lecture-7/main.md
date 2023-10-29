## Application Layer (Part 2)
## HTTP & The Web
The most popular network application is the World Wide Web, consisting of web browsers (clients) consisting of web servers; both these processes use [[HTTP - HyperText Transfer Protocol|HTTP]] - as specified by the IETF, as the application layer [[Protocol|protocol]]
## Web Cache
- Large amounts of communication over a network can be computationally expensive, and introduces congestion into the network
- The **goal** of a cache is to limit this by satisfying the client’s request without involving the origin server
### How It Works
- Web browsers can be configured to access the web via a cache
- If the required object is in the cache, it is simply returned; otherwise, the request is forwarded to the origin server
- Cache’s are typically used to serve popular requests since the [[Hit Ratio|hit ratio]] is higher, and hence makes the cache more effective
### Advantages
- Reduces network congestion
- Reduces response time for the client request
- Limits the amount of outgoing traffic from a network