# Selected Topics in Networking
## Network Interface
A **network interface** is the point of interconnection between a computer/device and a network
- Each network interface in the internet has a unique **IP address**
- A node can have multiple network interfaces e.g., for Wifi, Ethernet, etc.

A network interface is typically associated with a hardware **network interface card** (NIC)
- Each NIC has a unique **MAC address**
- The **loopback interface** (localhost) is a *virtual* network interface commonly used to test/debug network applications
	- It does not have hardware NIC
#### MAC Address Format
MAC addresses are 48-bit and denoted in hex digit pairs, delimited by a dash or semi-colon: e.g., `02:9B:B0:CB:AA:FC`
## Packet Structure
Packet structure is determined by the protocols in each layer of the TCP/IP stack. In each layer a header is added above the data given by the application layer, starting with the transport layer.
### Standardised Formats
#### Transport Layer (TCP)
![[Pasted image 20231105142810.png]]
#### Network Layer
![[Pasted image 20231105142826.png]]
#### Link Layer (Ethernet)
![[Pasted image 20231105142838.png]]
### SYN Attacks
A SYN attack is a denial-of-service attack in which an attacker floods a server with SYN packets from spoofed IPs, creating a large number of half-open connections thus taking up resources such that a normal user is denied a connection because the server is too busy

![[Pasted image 20231105143145.png]]

Note that a SYN packet is a packet in which the **only** flag that is set is the SYN flag.
## Address Resolution Protocol (ARP)
### Why do we need it?
Since the destination hardware address in a packet header needs to be changed at every intermediate node, routers need some way of determining the MAC address of the next router from it’s IP address (found in the routing table).
### Protocol Outline
To determine the MAC address corresponding to a particular IP address:
- A router sends an ARP request packet, consisting of:
	- A link layer header
	- An ARP header (containing the IP), to the reserved MAC address `FF:FF:FF:FF:FF:FF`
- This broadcasts the message to all directly connected routers
- The recipient whose IP address matches then replies with an ARP response containing their MAC address
- This address is stored within an ARP Cache for future use
### ARP Cache Poisoning
ARP cache poisoning is when an attacker exploits the fact that ARP allows for unsolicited replies by pretending to be the matching recipient; the router then sends the traffic to the attacker, allowing them unauthorised access to another recipient’s data. 