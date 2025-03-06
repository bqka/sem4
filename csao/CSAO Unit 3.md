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

# Instruction Formats

![[Pasted image 20250306061219.png|400]]

![[Pasted image 20250306061325.png|400]]

1. One Address Instruction
The instruction format in this type of computer uses one address field. For example, the instruction that specifies an arithmetic addition is defined by an assembly language instruction as ADD X where X is the address of the operand. The ADD instruction in this case results in the operation 
AC <--AC + M[X].
	accumulator type organization

![[Pasted image 20250306062450.png|300]]
2. Three/Two Address Instruction
general register type organization
![[Pasted image 20250306062329.png]]

Two Address
![[Pasted image 20250306062402.png|300]]

3. Zero Address Instruction
A stack-organized computer does not use an address field for the instructions ADD and MUL. The PUSH and POP instructions, however, need an address field to specify the operand that communicates with the stack.
TOS -> top of stack
![[Pasted image 20250306062526.png|400]]

# Addressing Modes

**Mode Field:** The mode field is used to locate the operands needed for the operation. There may or may not be an address field in the instruction. If there is an address field, it may designate a memory address or a processor register.
![[Pasted image 20250306062930.png|400]]

**Implied Mode**
- In this mode the operands are specified implicitly in the definition of the instruction. Ex. Complement Accumulator.
- All register reference instructions that use an accumulator are implied-mode instructions.
- Zero-address instructions in a stack-organized computer are implied-mode instructions since the operands are implied to be on top of the stack.

**Immediate Mode**
- In this mode the operand is specified in the instruction itself. In other words, an immediate-mode instruction has an operand field rather than an address field.

**Register Mode**
- In this mode the operands are in registers that reside within the CPU. The particular register is selected from a register field in the instruction. A k-bit field can specify any one of 2^k registers.

**Register Indirect Mode**
- In this mode the instruction specifies a register in the CPU whose contents give the address of the operand in memory.

**Auto increment/decrement Mode**
- This is similar to the register indirect mode except that the register is incremented or decremented after (or before) its value is used to access memory.
- When the address stored in the register refers to a table of data in memory, it is necessary to increment or decrement the register after every access to the table.

The **effective address** is defined to be the memory address obtained from the computation dictated by the given addressing mode.
The effective address is the address of the operand in a computational type instruction.

**Direct Address Mode**
- In this mode the effective address is equal to the address part of the instruction.

**Indirect Address Mode**
- In this mode the address field of the instruction gives the address where the effective address is stored in memory.

A few addressing modes require that the address field of the instruction be added to the content of a specific register in the CPU. The effective address in these modes is obtained from the following computation: 
effective address = address part of instruction + content of CPU register

**Relative Address Mode**
- In this mode the content of an index register is added to the address part of the instruction to obtain the effective address.

**Base Register Address Mode**
- In this mode the content of a base register is added to the address part of the instruction to obtain the effective address.

![[Pasted image 20250306064551.png|400]]
![[Pasted image 20250306064603.png|500]]
![[Pasted image 20250306064623.png|400]]

# Program Control

![[Pasted image 20250306065309.png|300]]

## Status Bit Conditions

![[Pasted image 20250306070341.png|500]]
![[Pasted image 20250306070428.png|400]]

![[Pasted image 20250306070505.png|500]]

## Subroutine Call and Return

A subroutine is a self-contained sequence of instructions that performs a given computational task.

The instruction is executed by performing two operations: 
(1) the address of the next instruction available in the program counter (the return address) is stored in a temporary location so the subroutine knows where to return, and 
(2) control is transferred to the beginning of the subroutine.
The last instruction of every subroutine, commonly called return from subroutine, transfers the return address from the temporary location into the program counter.

The most efficient way is to store the return address in a memory stack. The advantage of using a stack for the return address is that when a succession of subroutines is called, the sequential return addresses can be pushed into the stack

![[Pasted image 20250306071309.png|400]]

![[Pasted image 20250306071321.png|500]]