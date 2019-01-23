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


