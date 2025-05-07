![[Pasted image 20250507160940.png]]
![[Pasted image 20250507160951.png]]

![[Pasted image 20250507161623.png]]

**Control Word:** The control variables can be represented by a string of 1's and 0's called a control word.
![[Pasted image 20250507161739.png]]
![[Pasted image 20250428031256.png]]

![[Pasted image 20250428031531.png]]

a computer that employs microprogrammed control unit has two memories - main memory, control memory

user can store microprograms in main memory which can be altered
control memory holds a fixed microprogram which cannot be altered by the occasional user.

![[Pasted image 20250428031810.png]]

![[Pasted image 20250428031946.png]]

**Control Address Register**
![[Pasted image 20250428032055.png]]
![[Pasted image 20250428032151.png]]

**Sequencer**
![[Pasted image 20250428032227.png]]
![[Pasted image 20250428032316.png]]

**Pipeline Register**
![[Pasted image 20250428032346.png]]

## Address Sequencing

![[Pasted image 20250428033024.png]]

**Mapping**
![[Pasted image 20250428033241.png]]

![[Pasted image 20250428033341.png]]

![[Pasted image 20250428033559.png]]

![[Pasted image 20250428034830.png|500]]

![[Pasted image 20250428034859.png]]

**Subroutines**
![[Pasted image 20250428035029.png]]
![[Pasted image 20250428035117.png]]

## Microprogram example

![[Pasted image 20250428035311.png|500]]

**Microinstruction format**

![[Pasted image 20250428040219.png|400]]

![[Pasted image 20250428040300.png|400]]

in this example, control memory has 128 words (2^7) so AD has 7 bits

![[Pasted image 20250428040620.png]]

![[Pasted image 20250428040755.png]]
![[Pasted image 20250428040910.png]]

![[Pasted image 20250507133906.png|500]]
![[Pasted image 20250428040932.png|500]]

![[Pasted image 20250428041134.png]]


![[Pasted image 20250428041734.png]]
![[Pasted image 20250428041743.png]]
## The Fetch Routine

![[Pasted image 20250428041702.png]]
![[Pasted image 20250428041714.png]]
![[Pasted image 20250428041719.png]]

**Symbolic Microprograms**
![[Pasted image 20250428042053.png]]

![[Pasted image 20250428042814.png]]

this specifies the word content for the control memory

## Designing of Control Unit

**Decoding of microp fields**
![[Pasted image 20250428042951.png]]
![[Pasted image 20250428043154.png]]

**Microprogram sequencer**
![[Pasted image 20250428043320.png|450]]

![[Pasted image 20250428043544.png|400]]

the incrementer circuit is not a counter but rather a combinational circuit designed by cascading half-adder circuits