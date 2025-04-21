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

