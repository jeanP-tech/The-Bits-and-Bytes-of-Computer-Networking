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

TCP Control Flags and the Three-way Handshake
----------------
> The Six TCP Control Flags
  
URG(urgent)
- A value of one here indicates that the segment is considered urgent and that the urgent pointer field has more data about this
  
ACK(acknowleged)
- A value of one in this field means that the acknowlegement number field shoul be examined
  
PSH(push)
- The transmitting device wants the receiving device to push currently-buffered data to the application on the receiving end as soon as possible
  
RST (reset)
- One of the sides in a TCP connection hasn't been able to properly recover from a series of missing or malformed segments
  
SYN (synchronize)
- It's used when first establishing a TCP connection and makes sure the receiving end knows to examine the sequence number field
  
FIN (finish)
- When this flag is set to one, it means the transmitting computer doesn't have any more data to send and the connection can be closed
  
> Handshake
- A way for two devices to ensure that they're speaking the same protocol and will be able to understand each other

TCP Socket States
----------
Socket
- The instantiation of an end-point in a potential TCP connection
  
Instantiation
- The actual implementation of something defined elsewhere
  
LISTEN
- A TCP socket is ready and listening for incoming connections
  
SYN_SENT
- A synchronization request has been sent, but the connection hasn't been established yet
  
SYN-RECEIVED
- A socket previously in a LISTEN state has received a synchronization request and sent a SYN/ACK back
  
ESTABLISHED
- The TCP connection is in working order and both sides are free to send each other data
  
FIN_WAIT
- A FIN has been sent, but the corresponding ACK from the other end hasn't been received yet
  
CLOSE_WAIT
- The connection has been closed at the TCP layer, but that the application that opened the socket hasn't released its hold on the socket yet
  
CLOSED
- The connection has been fully terminated and that no further communication is possible
