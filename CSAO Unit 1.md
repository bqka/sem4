# Memory Transfer

## Memory Read
![[Pasted image 20250228072106.png]]

DR - Data Register
AR - Address Register

## Memory Write
![[Pasted image 20250228072218.png]]

R2' + 1 -> 2's complement

Net result: R3 <- R1 - R2

![[Pasted image 20250228072307.png|500]]

# Arithmetic Circuit

![[Pasted image 20250228073629.png|500]]
![[Pasted image 20250228073701.png|500]]
![[Pasted image 20250228074022.png]]

# Logic Microoperations

![[Pasted image 20250228074423.png]]
![[Pasted image 20250228074430.png]]

No. of Functions = 2^(2^n) ; n = number of variables
![[Pasted image 20250228074529.png]]
![[Pasted image 20250228074625.png|400]]

## Applications

![[Pasted image 20250228075056.png|500]]

AND -> Mask Operation: Clears bits of A where B is 0
![[Pasted image 20250228075304.png|200]]
OR -> Selective Set: sets 1 in A where B is 1
![[Pasted image 20250228075339.png|200]]
XOR -> Selective Complement sets 0 in A where B is 1
![[Pasted image 20250228075349.png|200]]
Selective Clear: Clears bits of A where B is 1
similar to mask, A = AB'
![[Pasted image 20250228075509.png|100]]
![[Pasted image 20250228075503.png|200]]

# Shift Microoperations

![[Pasted image 20250228080726.png|400]]

Logical Shift: serial inputs 0 to left/right
Circular Shift: rotates the bits left/right without loss of information
Arithmetic Shift: shifts SIGNED binary number to left/right

![[Pasted image 20250228080833.png|300]]
the signed bit remains same in arithmetic shift right

But in arithmetic shift left, if Rn-1 and Rn-2 are not same, the sign would be reversed, so we use an Overflow flag
![[Pasted image 20250228080912.png|150]]
![[Pasted image 20250228081021.png|500]]

![[Pasted image 20250228081103.png|500]]


