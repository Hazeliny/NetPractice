# Net Practice
Project as a general practical exercise to learn about networking and subnetting.

![imagen](https://raw.githubusercontent.com/xilen0x/xilen0x/master/images_x_repos/subnet.png)

reserved for private IP addresses:

192.168.0.0 – 192.168.255.255 (65,536 IP addresses)
172.16.0.0 – 172.31.255.255   (1,048,576 IP addresses)
10.0.0.0 – 10.255.255.255     (16,777,216 IP addresses)

102.198.231.0   | Reserved to represent the network address.
102.198.231.127 | Reserved as the broadcast address; used to send packets to all hosts of a network.

**Router**
Since the router separates different networks, the range of possible IP addresses on one of its interfaces must not overlap with the range of its other interfaces.

**Switch**
A switch connects multiple devices together in a single network. Unlike a router, the switch does not have any interfaces since it only distributes packets to its local network, and cannot talk directly to a network outside of its own.

**Concepts and Tips**
Communication between internet and users from bottom to top: Link layer -> Network layer -> Transport layer -> Application layer
TCP: Transport Layer
TCP stands for Transmission Control Protocol.
IP Address: Network Layer
internet service provider (ISP)
Internet Protocol version 4 (IPv4) defines an IP address as a 32-bit number. IP (IPv6), using 128 bits for the IP address, was standardized in 1998.
apply the mask to the IP address through a **bitwise AND** to find the network address of the IP
The mask can also be represented with the Classless Inter-Domain Routing (CIDR). This form represents the mask as a slash "/", followed by the number of bits that serve as the network address.

reserved for loopback: 127.0.0.0/8
