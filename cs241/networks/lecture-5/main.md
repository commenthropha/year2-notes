# Computer Network Basics
## Components
A network consists of 3 primary components:
1. [[Network Edge]]
2. [[Network Core]]
3. [[Communication Links]]
## Packet Delay
When transmitting [[Packets|packets]] over a computer network there are a number of sources of delay. Namely:
1. [[Transmission Delay]]
2. [[Queuing Delay]]
3. [[Nodal Processing]]
4. [[Propagation Delay]]

We can represent the total delay as a sum of the above sources:
	*d* = *dtrans* + *dqueue* + *dproc* + *dprop*

Packet delay is a significant factor affecting the [[Throughput|throughput]] at any given time
## Routing Network Traffic
When routing, we have a choice over how to manage network traffic between:
- [[Packet Switching]]
- [[Circuit Switching]]

- Internet traffic is bursty in nature, hence utilisation for any given [[Flow|flow]] is inconsistent
- Packet Switching is hence preferable to Circuit Switching as it makes idle routes available to other [[Flow|flows]], and allows a [[Flow|flow]] to use alternative routes if any given route is congested/fails
	- This allows us to take advantage of a larger fraction of the overall [[Throughput|throughput]]
## Layering
We can broadly abstract network functions into layers, which we collectively term the [[Internet Protocol Stack|internet protocol stack]]
### Advantages
Modelling network functions in this way helps to separate concerns
- In other words, it makes it easier to add services to a layer or change its implementation without affecting other layers