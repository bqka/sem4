![[Pasted image 20250303011001.png|400]]

# General Register Organization

![[Pasted image 20250303011255.png|500]]

![[Pasted image 20250303011134.png|500]]

![[Pasted image 20250303011442.png|500]]

## Control Word

![[Pasted image 20250303012346.png|400]]
![[Pasted image 20250303012429.png]]

![[Pasted image 20250303012458.png|350]]
0 - Transfer A 
1 - Increment A
2 - add A + B
5 - subtract A - B
6 - decrement A
8 - AND A and B
10 - OR A and B
12 - XOR A and B
14 - Complement A
16 - SHR A 
24 - SHL A
### Example

![[Pasted image 20250303012657.png|150]]
![[Pasted image 20250303012713.png|400]]
![[Pasted image 20250303013840.png]]
![[Pasted image 20250303013833.png]]
![[Pasted image 20250303013821.png]]

# Stack Organization

## Register Stack

![[Pasted image 20250303014135.png|350]]

when pop operation, SP is decremented
when push operation, SP is incremented and the new word is written

![[Pasted image 20250303014310.png|600]]

initially, EMPTY is 1 and FULL is 0

Push operation
![[Pasted image 20250303014339.png|500]]
![[Pasted image 20250303014411.png|500]]

for 64 word stack, max bit representation is 0-63, so when 63 + 1 = 0000000 so if SP+1 = 0, the stack is full

Pop operation
![[Pasted image 20250303014546.png|500]]
## Memory Stack

A stack can exist as a stand-alone unit as in Fig. 8-3 or can be implemented in a random-access memory attached to a CPU. The implementation of a stack in the CPU is done by assigning a portion of memory to a stack operation and using a processor register as a stack pointer.

![[Pasted image 20250303014621.png|400]]
![[Pasted image 20250303014816.png]]
![[Pasted image 20250303014849.png]]

Push and pop
![[Pasted image 20250303014951.png]]

to check stack overflow/underflow, we compare the Stack pointer with the upper-limit register (3000 in this case) after a push operation and lower-limit register (4001 in this case) after a pop operation