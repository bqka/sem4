# Register Transfer Language
![[csao/syllabus.png]]

A **Microoperation** is an elementary operation performed on the information stored in one or more registers.

![[Pasted image 20250306034326.png]]

## Register Transfer

![[Pasted image 20250306034615.png|400]]

Information transfer from one register to another is shown as 
$$ R_2 \leftarrow R_1$$
contents of R2 are replaced by R1, contents of R1 do not change

A **Control Function** is a boolean variable that is equal to 0 or 1 
![[Pasted image 20250306034756.png|150]]

![[Pasted image 20250306034819.png|300]]

the control variable is synchronized w the same clock as the one applied to the register
# Bus & Memory Transfers

A more efficient scheme for transferring information between registers in a multiple-register configuration is a common bus system. A bus structure consists of a set of common lines, one for each bit of a register, through which binary information is transferred one at a time.

![[Pasted image 20250306035216.png|500]]

## Three State Bus Buffers

Two of the states are signals equivalent to logic 1 and 0 as in a conventional gate. The third state is a high-impedance state. The high-impedance state behaves like an open circuit, which means that the output is disconnected and does not have a logic significance.

![[Pasted image 20250306035400.png|400]]
![[Pasted image 20250306035410.png|300]]
## Memory Transfers

**Memory Read**
![[Pasted image 20250228072106.png]]
DR - Data Register
AR - Address Register

**Memory Write**
![[Pasted image 20250228072218.png]]
R2' + 1 -> 2's complement
Net result: R3 <- R1 - R2

![[Pasted image 20250228072307.png|500]]

## Binary Adder

![[Pasted image 20250306035759.png|400]]
full adders in cascade
n bit binary adders -> n full adders
## Binary Adder Subtractor

![[Pasted image 20250306035930.png|400]]
When M = 0, we have B xor 0 = B. The full-adders receive the value of B, the input carry is O, and the circuit performs A plus B. When M = 1, we have B xor 1 = B' and C0 = 1. The B inputs are all complemented and a 1 is added through the input carry.
-> a + 2's complement of b = a - b
## Binary Incrementer

![[Pasted image 20250306040042.png|400]]
## Arithmetic Circuit

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

# Arithmetic Logic Shift Unit

![[Pasted image 20250306040537.png|400]]

![[Pasted image 20250306040657.png|400]]