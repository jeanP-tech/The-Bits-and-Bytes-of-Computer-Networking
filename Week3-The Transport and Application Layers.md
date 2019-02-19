The Transport Layer
=============

The transport layer
---------

The transport layer has the ability to multiplex and demultiplex
- Multiplexing means that nodes on the network have the ability 

- The transport layer handles multiplexing and demultiplexing through ports

Port
- A 16-bit number that's used to direct traffic to specific sercices running on a networked computer

- Different network services run while listening on specific ports for incoming requests

Dissection of a TCP Segment
------------
TCP segment
- Made up of a TCP header and a data section

A TCP header itself is split into lots of fields.

Destination port
- The port of the service the traffic is intended for 
  
Source port
- A high-numbered port chosen from a special section of ports known as ephemeral ports
  
Sequence number
- A 32-bit number that's used to keep track of where in a sequence of TCP segments this one is expected to be
  
Achnowledgement number
- The number of the next expected segment  
  
Data offset field
- A 4 - bit number that communicates how long the TCP header for this segment is  
  
TCP window
- Specifies the range of sequence numbers that might be sent before an acknowledgement is required
  
TCP checksum
- Operates just like the checksum fields at the IP and ethernet level
  
Urgent pointer field
- Used in conjunction with one of the TCP control fags to point out particular segments that might be more important than others
  
Options field
- It is sometimes used for more complicated flow control protocols
