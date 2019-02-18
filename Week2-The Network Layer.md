The Network Layer
==========


The Network Layer
-----------

IP Addresses
-----------

IP addresses are 32-bit long numbers made up of 4 octets, and each octet is normally described in decimal numbers.  
  
8 bits of data, or a single octet, can represent all decimal numbers from 0 to 255.  
  
IP addresses belong to networks, not to the devices attached to those networks.  
  
In most cases, static IP addresses are reserved for servers and network devices, while dynamic IP addresses are reserved for clients.

IP Datagrams and Encapsulation
-----------------

IP datagram: A highly structured series of fields that are strictly defined.  
  
The most common version of IP is version 4, or IPv4  
  
Header Lengly field: Alomost always 20 bytes in length when dealing with IPv4  
  
Service Type field: These 8 bits can be used to specify details about quality of service, or QoS, technologies  
  
Total Length field: Indicates the total length of the IP datagram it's attached to  
  
Identification field: A 16-bit number that's used to group messages together  
  
The maximum size of a single datagram is the largest number you can represent with 16 bits: 65,535  
  
If the total amount of data that needs to be sent is larger than what can fit in a single datagram, the IP layer needs to split this data up into many individual packets.  
  
Flag field: Used to indicate if a datagram is allowed to be fragmented, or to indicate that the datagram has already been fragmented   
Fragmentation: The process of taking a single IP datagram and splitting it up into several smaller datagrams   
  
Time to Live (TTL) field: An 8-bit field that indicates how many router hops a datagram can traverse before it's thrown away  
  
Protocol field: Another 8-bit field that contains data about what transport layer protocol is being used  
  
Header checksum field: A checksum of the contents of the entire IP datagram header  
  
IP options field: An optional field and is used to set special characteristics for datagrams primarily used for testing purposes  
  
Padding field: A series of zeros used to ensure the header is the correct total size

IP Address Classes
------------
IP addresses can be split into two sections: the network ID and the host ID  
ex) 9.100.100.100  
9 - network ID  
100.100.100 - host ID  
  
Address class system: A way of defining how the global IP address space is split up

Address Resolution Protocol
-----------------------

ARP: A protocol used to discober the hardware address of a node with a certain IP address  
  
ARP table: A list of IP addresses and the MAC addresses associated with them  
  
ARP table entries generally expire after a short amount of time to ensure changes in the network are accounted for.

Subnetting
======

subnetting: The process of taking a large network and splitting it up into many individual and smaller subnetworks, or subnets

Baxic Binary
--------
- 8 bit : 2^8 = 256
- 4 bit : 2^4 = 16
- 16 bit : 2^16 = 65536
  
- Two of the most important operators are OR and AND  
- In computer logic, a 1 represents true and a 0 represents false  
  
X OR Y = Z  
"If either X or Y is true, then Z is true; otherwise, it's false."  
1 OR 0 = 1  
0 OR 0 = 0  
  
Subnet mask :  A way for a computer to use and operators to determine if an IP address exists on the same network

CIDR
---------
Network ID
- 8 bit : Class A
- 16 bit : Class B
- 24 bit : Class C
The sizing of these networks aren't always appropriate for the needs of most businesses  
  
Demarcate : To set something off when discussing computer networking  
  
Demarcation point: To describe where one network or system ends and another one begins

Routing
======

Basic Routing Concepts
-------------

Router : A network device that forwards traffic depending on the destination address of that traffic  
  
Basic Routing:
1. Receive data packet
2. Examines destination IP
3. Looks up IP destination network in routing table
4. Forwards traffic to destination

Routing tables
-----------

The most basic routing table will have four columns
1. Destination network
2. Next hop
3. Total hops
4. Interface

Interior Gateway Protocols
------------

Routing protocols  
- Special protocols the routers use to speak to each other in order to share what information they might have
- Routing protocols fall into two main categories: interior gateway protocols and exterior gateway protocols
- Interior gateway protocols are further split into two categories: Link state routing protocols and distance-vector protocols.

Interior gateway protocols
- Used by routers to share information within a single autonomous system

Autonomous system
- A collection of networks that all fall under the control of a single network operator
  
The two main types of interior gateway protocols are link state routing protocols and distance-vector protocols  
  
In computer science, a list is known as a vector  
  
- **Distance vector protocols** are pretty simple.
	- But they don't allow for a router have much information about the state of the world outside of their own direct neighbors.
	- Becuase a router might be slow to react to a change in the network far away from it
- Routers using a **link-state protocol** take a more sophisticated approach to determining the best path to a network  
	- Linked state protocols got their name because each router advertises the state of the link of each of its interfaces
	- Every router on the system knows every detail about every other router in the system
	- Link state protocols require both more memory in order to hold all of this data

Exterior Gateway Protocols
-----------

Internet Assigned Numbers Authority(IANA)
- A non-profit organization that helps manage things like IP address allocation

- Along with managing IP address allocation, the IANA is also responsible for ASN, or Autonomous System Number allocation.

Autonomous System Number(ASN)
- Numbers assigned to individual autonomous system

Non-Routable Address Space
--------------

- When IP was first defined, it defined an IP address as a single 32-bit number.  
- A single 32-bit number can represent 4,294,967,295
- However, the IPv4 standard doesn't even have enough IP addresses available for every person on the planet
- In 1996, RFC 1918 was published
- RFC stands for Request for Comments
- RFC 1918, outlined a number of networks that would be defined as non-routable address space
	- They are ranges of IPs set aside for use by anyone that cannot be routed to.
- RFC 1918 defined three ranges of IP addresses
