![[Pasted image 20250307052213.png]]
![[Pasted image 20250307052341.png]]
![[Pasted image 20250307052420.png]]
Flow Control
Access Control
Error Control - detection, correction

![[Pasted image 20250307052700.png]]
![[Pasted image 20250307052822.png]]
![[Pasted image 20250307052856.png]]
![[Pasted image 20250307052937.png|400]]

# Framing

![[Pasted image 20250307053403.png]]
![[Pasted image 20250307053441.png]]
![[Pasted image 20250307053257.png]]
![[Pasted image 20250307053539.png]]
Framing approaches - bit oriented, byte oriented
![[Pasted image 20250307053712.png]]
bit oriented protocol - HDLC Highilevel data link control
clock based framing - SONET protocol -> synchronous optical network
![[Pasted image 20250307053750.png]]
![[Pasted image 20250307053805.png]]

# Flow Control Protocols
![[Pasted image 20250307054537.png]]
ARQ - automatic repeat request
## Stop and Wait
![[Pasted image 20250307054640.png]]
![[Pasted image 20250307054658.png]]
![[Pasted image 20250307054708.png|300]]
![[Pasted image 20250307054723.png]]
![[Pasted image 20250307054739.png]]
![[Pasted image 20250307054755.png]]

## Stop and Wait ARQ
![[Pasted image 20250307054843.png]]
![[Pasted image 20250307054854.png]]
![[Pasted image 20250307054930.png]]
![[Pasted image 20250307055149.png]]
## Sliding Window

![[Pasted image 20250307055206.png]]
![[Pasted image 20250307055354.png]]

### Go Back N ARQ
N is the sender window size
![[Pasted image 20250307055554.png]]
![[Pasted image 20250307055641.png]]
![[Pasted image 20250307055932.png]]

### Selective Repeat ARQ

![[Pasted image 20250307060730.png]]
![[Pasted image 20250307060859.png]]
![[Pasted image 20250307061004.png]]
Tp -> propogation delay
Tt -> total time
![[Pasted image 20250307061136.png|300]]
![[Pasted image 20250307061516.png]]

# Bit and Byte Stuffing
![[Pasted image 20250307061939.png]]
![[Pasted image 20250307061946.png]]
![[Pasted image 20250307062047.png]]
Bit stuffing 
adding 0

# Error Detection
![[Pasted image 20250307062229.png|400]]
![[Pasted image 20250307062746.png]]
VRC, LRC -> parity check

## VRC
![[Pasted image 20250307063020.png|400]]
![[Pasted image 20250307062854.png]]
![[Pasted image 20250307063007.png]]

## LRC
![[Pasted image 20250307063154.png]]
![[Pasted image 20250307063258.png]]
![[Pasted image 20250307063501.png]]

## Checksum

![[Pasted image 20250307063606.png|400]]
![[Pasted image 20250307063709.png]]
![[Pasted image 20250307063804.png]]
![[Pasted image 20250307063940.png]]
this is what is sent to the receiver
![[Pasted image 20250307063958.png]]
![[Pasted image 20250307064035.png]]
![[Pasted image 20250307064054.png]]
![[Pasted image 20250307064113.png]]
if error involved does not change in sum, then no error is detected

## CRC
Cyclic Redundancy Check
![[Pasted image 20250307064309.png]]
![[Pasted image 20250307064551.png]]
on receiver side, the receiver divides the data with the divisor
![[Pasted image 20250307064848.png]]

## Hamming Code

hamming distance
![[Pasted image 20250307065445.png|400]]

XOR of two code words
minimum hamming distance = d (min value of xor of 2 code words)
can detect error of d-1 bits

if i have 7 bit hamming code, 4 bits are data and 3 bits are parity
![[Pasted image 20250307065634.png]]
3 parity bits,
which position? 2^n position
=> bit 1, bit 2, bit 4, bit 8 etc.

![[Pasted image 20250307070605.png]]


# Multiple Access Protocols

![[Pasted image 20250307071447.png]]
![[Pasted image 20250307072220.png]]
![[Pasted image 20250307072323.png]]
![[Pasted image 20250307072358.png]]
![[Pasted image 20250307101227.png|400]]
![[Pasted image 20250307101244.png|400]]
![[Pasted image 20250307072414.png]]
![[Pasted image 20250307101316.png|400]]
![[Pasted image 20250307101326.png|400]]

## Pure Aloha

![[Pasted image 20250307072517.png]]
![[Pasted image 20250307072622.png]]
![[Pasted image 20250307073027.png]]
![[Pasted image 20250307072716.png]]

## Slotted Aloha
![[Pasted image 20250307073303.png]]
![[Pasted image 20250307073339.png]]
![[Pasted image 20250307073228.png]]
![[Pasted image 20250307073348.png]]

![[Pasted image 20250307073414.png]]

## CSMA

![[Pasted image 20250307073725.png]]
![[Pasted image 20250307073743.png]]
![[Pasted image 20250307073901.png]]
![[Pasted image 20250307073914.png]]
![[Pasted image 20250307074034.png]]
![[Pasted image 20250307074209.png]]
![[Pasted image 20250307074308.png]]
![[Pasted image 20250307074325.png]]
## CSMA/CD

![[Pasted image 20250307074437.png]]
![[Pasted image 20250307075233.png]]

TT >= 2 * PD
TT = L / BW
PD = D / velocity
## CSMA/CA

![[Pasted image 20250307075517.png]]
![[Pasted image 20250307075949.png]]
![[Pasted image 20250307080351.png]]

# IEEE 802.5

![[Pasted image 20250307081708.png]]

- ring topology
- piggybacking acknowledgement is used
- differential manchester encoding is used

![[Pasted image 20250307082357.png]]
all values in byte
Start Delimiter - used for synchronizatoin
AC - access control
FC - frame control
End Delimiter
FS - frame status
# IEEE 802.3
![[Pasted image 20250307081751.png]]
![[Pasted image 20250307081854.png]]
SFD - 10101011