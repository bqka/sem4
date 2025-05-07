A computer instruction is a binary code that specifies a sequence of microoperations for the computer. Instruction codes together with data are stored in memory.
- The computer reads each instruction from memory and places it in a control register.
- The control then interprets the binary code of the instruction and proceeds to execute it by issuing a sequence of microoperations.

An **instruction code** is a group of bits that instruct the computer to perform a specific operation.

![[Pasted image 20250228210137.png]]

![[Pasted image 20250228210206.png]]

**Role of Control Unit**

The control unit receives the instruction from memory and interprets the operation code bits. It then issues a sequence of control signals to initiate microoperations in internal computer registers. For every operation code, the control issues a sequence of microoperations needed for the hardware implementation of the specified operation.
# Stored Program Organization

![[Pasted image 20250228211936.png]]

if we have 4096 words, we need 12 bits for address since 2^12 = 4096

- control unit reads 16 bit instruction from program portion of memory
- uses 12 bit address part to read a 16 bit operand from memory
- performs the operation specified by opcode

![[Pasted image 20250228211133.png|400]]

![[Pasted image 20250228212139.png]]

## Indirect Address

15th bit is Mode
mode = 0 -> direct address
mode = 1 -> indirect address

![[Pasted image 20250228212504.png|500]]

# Computer Registers

![[Pasted image 20250228213034.png|500]]

AC is a processor register which holds the results of addition, subtraction, etc. it has 16 bits as the operations are performed on binary operands of 16 bits
AR has 12 bits since this is the width of memory address
PC has 12 bits as it holds the address of the next instruction

**Branch Instruction and working**
![[Pasted image 20250228213336.png]]

![[Pasted image 20250228213403.png|350]]

![[Pasted image 20250228213506.png]]

![[Pasted image 20250228215322.png]]
![[Pasted image 20250228215036.png]]

# Computer Instructions

- memory reference instruction
	- I is addressing mode direct (0)/indirect (1)
- register reference instruction
- input output instruction

![[Pasted image 20250228215838.png|400]]

Basic computer has 25 instructions

![[Pasted image 20250228220330.png]]

![[Pasted image 20250228221138.png|450]]

![[Pasted image 20250306085625.png|500]]
## Instruction Set Completeness

![[Pasted image 20250228234304.png]]

# Timing and Control

![[Pasted image 20250228234843.png|400]]
![[Pasted image 20250301000434.png]]

![[Pasted image 20250306044150.png|200]]
![[Pasted image 20250306044023.png|500]]
# Instruction Cycle

![[Pasted image 20250301001001.png|500]]
![[Pasted image 20250301002303.png|500]]
![[Pasted image 20250301001428.png|500]]
![[Pasted image 20250301002842.png|500]]
![[Pasted image 20250301005044.png]]
![[Pasted image 20250306050024.png]]
for RRI, D7 = 1, I = 0
![[Pasted image 20250301005649.png|500]]
# Design of Accumulator Logic

![[Pasted image 20250301010822.png|500]]
![[Pasted image 20250301011557.png|400]]
p = D7 I T3
## Control of AC Register

![[Pasted image 20250301011508.png|500]]

## Adder and Logic Circuit

![[Pasted image 20250301012448.png|500]]