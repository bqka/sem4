# Assembly

![[Pasted image 20250301020219.png]]

![[Pasted image 20250301020252.png|500]]
![[Pasted image 20250301020243.png|500]]

=> 83 - (-23)
Minuend - Subtrahend
![[Pasted image 20250301020320.png|400]]
## Translation to Binary

![[Pasted image 20250301041613.png|500]]
![[Pasted image 20250301041626.png|300]]

**Pseudo instruction**
![[Pasted image 20250301040408.png|500]]
![[Pasted image 20250301040401.png|600]]

**Address Symbol Table**
![[Pasted image 20250301041742.png]]
![[Pasted image 20250301041809.png|300]]
![[Pasted image 20250301041834.png|500]]
# The Assembler

![[Pasted image 20250301041308.png|450]]

**Important**
A is 41 (65 in binary)
0 is 30 (48 in binary)
(space) is 20
, is 2C
CR is 0D

- if a label symbol has less than 3 characters, the memory locations are filled with code for space 
## First Pass
![[Pasted image 20250301041242.png|500]]
![[Pasted image 20250301041035.png|400]]

Since each word is 16 bits and a character has 8 bits, 1 word can hold 2 characters

![[Pasted image 20250301043739.png|500]]
## Second Pass

![[Pasted image 20250301044103.png]]

![[Pasted image 20250301041102.png|500]]

![[Pasted image 20250301044613.png]]

