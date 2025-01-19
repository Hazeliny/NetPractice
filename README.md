# Net Practice
Project as a general practical exercise to learn about networking and subnetting.

![imagen](https://raw.githubusercontent.com/xilen0x/xilen0x/master/images_x_repos/subnet.png)

**reserved for private IP addresses:**


192.168.0.0 – 192.168.255.255 (65,536 IP addresses)

172.16.0.0 – 172.31.255.255   (1,048,576 IP addresses)

10.0.0.0 – 10.255.255.255     (16,777,216 IP addresses)


Example:

IP address   |   102.198.231.125

mask         |   255.255.255.128      ===>    255.255.255.10000000

apply the mask to the IP address through a **bitwise AND** to find the network address of the IP

network address    |    102.198.231.0

so possible IP addresses range is: 102.198.231.1(0000000 ~ 1111111), i.e. 102.198.231.0 ~ 102.198.231.127

( Reserved to represent the **network address**    |    102.198.231.0 )

( Reserved as the **broadcast address**; used to send packets to all hosts of a network    |    102.198.231.127 )

( Reserved as gateway address  |  102.198.231.1 )

So, available IP addresses are: 102.198.231.2 ~ 102.198.231.126


**Router**

Since the router separates different networks, the range of possible IP addresses on one of its interfaces must not overlap with the range of its other interfaces.



**Switch**

A switch connects multiple devices together in a single network. Unlike a router, the switch does not have any interfaces since it only distributes packets to its local network, and cannot talk directly to a network outside of its own.



**Concepts and Tips**

Communication between internet and users from bottom to top: **Link layer -> Network layer -> Transport layer -> Application layer**

TCP: Transport Layer

TCP stands for Transmission Control Protocol.

IP Address: Network Layer

internet service provider (ISP)

Internet Protocol version 4 (IPv4) defines an IP address as a 32-bit number. IP (IPv6), using 128 bits for the IP address, was standardized in 1998.

The mask can also be represented with the Classless Inter-Domain Routing (CIDR). This form represents the mask as a slash "/", followed by the number of bits that serve as the network address. /30 means the first 30 bits of IP address present network address, and the last 2 bits present host address.

**Switch** hasn't interface, it only distributes packets to its local network, can't talk directly to a network outside of its own; while **router** has interface, which is used to connect all the networks, the IP addresses on the interface can not overlap those on other interfaces.

**Routing table** exists on router and network host:

(Router)  (Destination) 0.0.0.0/0  ===>  93.198.15.253 (next hop)    next hop means the IP address of next router on the packet's way.

subnet mask is to distinguish between a network address and a host address in IP address.

reserved for **loopback**: 127.0.0.0/8


In TCP and UDP, a port number is represented by a 16-bit unsigned integer, and there are three types of ports.

Ports 0 to 1023 are reserved for specific services and protocols, such as HTTP (port 80), FTP (port 21), and SSH (port 22). They require administrative privileges to use

Ports numbered 1024 to 49151 can be registered for specific purposes and are used by non-standard applications and services.

Dynamic or private ports (49152 to 65535) are used by client applications for outgoing connections. These ports are dynamically allocated by the operating system to clients when they initiate outgoing connections.

