Responsibilties of TRANSPORT LAYER
1. End to end delivery of data. (port to port delivery) 
2. Reliability ( We prefer TCP to UDP as TCP establishes a connection oriented now and the data sent by the TCP is received by the receiver in order sequence. 
3. Error Control( checksum) 
4. Congestion and Flow control ( STOP & WAIT ; GO BACK & SR) 
5. Segmentation ( data from APP layer comes in bits which are transformed into a SEGMENT through tcp/ udp and then sent it to the Network Layer. 
6. Multiplex and DEMUX.

![[Pasted image 20250420230929.png]]

![[Pasted image 20250420233039.png]]
![[Pasted image 20250420235202.png]]

TCP uses 3 way handshake
![[Pasted image 20250421000128.png]]
![[Pasted image 20250421000117.png]]

![[Pasted image 20250421001626.png]]
![[Pasted image 20250421002840.png|300]]

UDP

Connectionless protocol
packets have no order

![[Pasted image 20250421013601.png]]
![[Pasted image 20250421013933.png]]

![[Pasted image 20250421014827.png]]

tcp - http, ftp
udp - dns, bootp, dhcp (dynamic host control protocol), rip (routing information protocol)

# TCP

The Transmission Control Protocol is the most common transport layer protocol. It works together with IP and provides a reliable transport service between processes using the network layer service provided by the IP protocol.   
The various **services** provided by the TCP to the application layer are as follows:   
 

1. **Process-to-Process Communication –**   
    TCP provides a process to process communication, i.e, the transfer of data that takes place between individual processes executing on end systems. This is done using port numbers or port addresses. Port numbers are 16 bits long that help identify which process is sending or receiving data on a host.   
     
2. **Stream oriented –**   
    This means that the data is sent and received as a stream of bytes(unlike UDP or IP that divides the bits into datagrams or packets). However, the network layer, that provides service for the TCP, sends packets of information not streams of bytes. Hence, TCP groups a number of bytes together into a _segment_ and adds a header to each of these segments and then delivers these segments to the network layer. At the network layer, each of these segments is encapsulated in an IP packet for transmission. The TCP header has information that is required for control purposes which will be discussed along with the segment structure.   
     
3. **Full-duplex service –**   
    This means that the communication can take place in both directions at the same time.   
     
4. **Connection-oriented service –**   
    Unlike UDP, TCP provides a connection-oriented service. It defines 3 different phases: 
    - Connection establishment
    - Data transfer
    - Connection termination
5. **Reliability –**   
    TCP is reliable as it uses checksum for error detection, attempts to recover lost or corrupted packets by re-transmission, acknowledgement policy and timers. It uses features like byte number and sequence number and acknowledgement number so as to ensure reliability. Also, it uses congestion control mechanisms.   
     
6. **Multiplexing –**   
    TCP does multiplexing and de-multiplexing at the sender and receiver ends respectively as a number of logical connections can be established between port numbers over a physical connection.

![[Pasted image 20250509142639.png]]

The header of a TCP segment can range from 20-60 bytes. 40 bytes are for options. If there are no options, a header is 20 bytes else it can be of upmost 60 bytes.   
Header fields:   
 

- **Source Port Address –**   
    A 16-bit field that holds the port address of the application that is sending the data segment.   
     
- **Destination Port Address –**   
    A 16-bit field that holds the port address of the application in the host that is receiving the data segment.   
     
- **Sequence Number –**   
    A 32-bit field that holds the sequence number, i.e, the byte number of the first byte that is sent in that particular segment. It is used to reassemble the message at the receiving end of the segments that are received out of order.   
     
- **Acknowledgement Number –**   
    A 32-bit field that holds the acknowledgement number, i.e, the byte number that the receiver expects to receive next. It is an acknowledgement for the previous bytes being received successfully.   
     
- **Header Length (HLEN) –**   
    This is a 4-bit field that indicates the length of the TCP header by a number of 4-byte words in the header, i.e if the header is 20 bytes(min length of TCP header), then this field will hold 5 (because 5 x 4 = 20) and the maximum length: 60 bytes, then it’ll hold the value 15(because 15 x 4 = 60). Hence, the value of this field is always between 5 and 15.   
     
- **Control flags –**   
    These are 6 1-bit control bits that control connection establishment, connection termination, connection abortion, flow control, mode of transfer etc. Their function is: 
    - URG: Urgent pointer is valid
    - ACK: Acknowledgement number is valid( used in case of cumulative acknowledgement)
    - PSH: Request for push
    - RST: Reset the connection
    - SYN: Synchronize sequence numbers
    - FIN: Terminate the connection
- **Window size –**   
    This field tells the window size of the sending TCP in bytes.   
     
- **Checksum –**   
    This field holds the checksum for error control. It is mandatory in TCP as opposed to UDP.   
     
- **Urgent pointer –**   
    This field (valid only if the URG control flag is set) is used to point to data that is urgently required that needs to reach the receiving process at the earliest. The value of this field is added to the sequence number to get the byte number of the last urgent byte.

![[Pasted image 20250509143341.png]]

![[Pasted image 20250509143616.png]]
![[Pasted image 20250509143601.png]]

![[Pasted image 20250509144814.png]]

# UDP

![[Pasted image 20250509145059.png]]

- ****Source Port:**** Source Port is a 2 Byte long field used to identify the port number of the source.
- ****Destination Port:**** It is a 2 Byte long field, used to identify the port of the destined packet.
- ****Length:**** Length is the length of UDP including the header and the data. It is a 16-bits field.
- ****Checksum:**** Checksum is 2 Bytes long field. It is the 16-bit one’s complement of the one’s complement sum of the UDP header, the pseudo-header of information from the IP header, and the data, padded with zero octets at the end (if necessary) to make a multiple of two octets.

****Notes –**** Unlike TCP, the Checksum calculation is not mandatory in UDP. No Error control or flow control is provided by UDP. Hence UDP depends on IP and ICMP for error reporting. Also UDP provides port numbers so that is can differentiate between users requests.

# Congestion Control

![[Pasted image 20250509152752.png]]
![[Pasted image 20250509152807.png]]
![[Pasted image 20250509153158.png]]

