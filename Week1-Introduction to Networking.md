The TCP/IP Five-Layer Network Model
=====================

The TCP/IP Five-Layer Network Model
-----------

Physical layer  
:Represents the physical devices that interconnect computers

Data link layer  
: Responsible for defining a common way of interpreting these signals so network devices can communicate  
  
The Ethernet standards also define a protocol responsible for getting data to nodes on the same network or link.

Network layer  
: Allows different networks to communicate with each other through devices known as routers  
  
**IP** is the heart of the Internet and most smaller networks around the world.  
  
Transport layer  
: Sorts out which client and server programs are supposed to get that data  
  
Physical layer is the delivery truck and the roads.  
The data link layer is how the delivery trucks get from one intersection to the next over and over.  
The network layer identifies which roads need to be taken to get from addrss A to address B.  
The transport layer ensures that delivery driver knows how to knock on your door to tell you your package has arrived.  
And the application layer is the contents of the package itself.

The Basics of Networking Devices
==============

Cables
-----------

Cables: Connect different devices to each other, allowing data to be transmitted over them

two categories
- Copper
	- most common
	- The most common forms of copper twisted-pair cables used in networking are Cat5, Cat5e, and Cat6 cables.
	- Crosstalk: When an electrical pulse on one wire is accidentally detected on another wire
- Fiber: Contain indibidual optical fibers, which are tiny tubes made out of glass about the width of a human hair

Hubs and Switches
-----------

Hub: A physical layer device that allows for connections from many computers at once  
  
Collision domain: A network segment where only one device can communicate at a time.  
If multiple systems try sending data at the same time, the electrical pulses sent across the cable can interfere with each other.

Routers
-----


Hubs and switches: The primary devices used to connect computers on a single network, usually referred to as a LAN, or local area network  
  
Router: A device that knows how to forward data between independent networks  
  
Border Gateway Protocol(BGP): Routers share data with each other via this protocol, which lets them learn about the most optimal paths to forward traffic  

The physical Layer
==============

Moving Bits Across the Wire
-------

The physical layer consists of devices and means of transmitting bits across computer networks.  
  
Bit: The samllest representation of data that a computer can understand; it's a one or a zero  
  
Ones and zeros are sent cross those network cabes through a process called modulation.  
  
Modulation: A way of varying the voltage of this charge moving across the cable  
  
Twisted Pair Cabling and Duplexing
-------------

Duplex communication: The concept that information can flow in both directions across the cable  
ex) A phone call  
  
Simplex communication: This process is unidirectional  

Network Ports and Patch Panels
---------------

Network ports are generally directly attached to the devices that make up a computer network

The Data Link Layer
------------

CSMA/CD: Used to determine when the communications channels are clear, and when a device is free to trasmit data  
  
MAC address: A globally unique identifier attached to and individual network interface  
  
It's a 48-bit number normally represented by six groupings of two hexadecimal numbers.  
  
Hexadecimal: A way to represent numbers using 16 digits  
  
Octet: In computer networking, any number that can be represented by 8 bits  
  
Organiztionally Unique Identifier(OUI): The first three octets of a MAC address   
  
Unicast, Multicast, and Broadcast: A uniast transmission is always meant for just one receiving address  
  
If the least significant bit in the first octet of a destination address is set to zero, it means that ethernet frame is intended for only the destination address.  
  
If the least significant bit in the first octet of a destination address is set to one, it means you're deling with a multicast frame.  

Disscting an Ethernet Frame
-----------

Data packet: An all-encompassing term that represents any single set of binary data being sent across a network link  
  
Ethernet frame: A highly structured collection of information presented in a specific order  
  
Preamble: 8 bytes (or 64 bits) long, and can itself be split into two sections  
  
Start frame delimiter(SFD): Signals to a receiving device that the preamble is over and that the actual frame contents will now follow  
  
Destination MAC address:The hardware address of the intended recipient  
  
Ether Type field: 16 bits long and used to describe the protocol of the contents of the frame  
  
VLAN header: Indicates that the frame itself is what's called a VLAN frame  
If a VLAN header is present, the EtherType field follows it.  
  
Virtual LAN(VLAN): A technique that lets you have multiple logical LANs operating on the same physical equipment  
  
Payload: In networking terms, is the actual data being transported, which is everything that isn
t a header  
  
Frame Check Sequence: A 4-byte(or 32-bit) number that represents a checksum value for the entire frame  
This checksum value is calculated by performing what's known as a cyclical redundancy check against the frame.  
  
Cyclical Redundancy Check (CRC): An important concept for data integrity , and is used all over computing, not just network trasmissions




