## Peripheral Devices

![[Pasted image 20250428234037.png]]
![[Pasted image 20250428234122.png]]

**ASCII**
![[Pasted image 20250428234224.png]]
![[Pasted image 20250428234240.png]]

## IO Interface

![[Pasted image 20250428234358.png]]
![[Pasted image 20250428234346.png]]

![[Pasted image 20250428234519.png]]

![[Pasted image 20250428234626.png|500]]
![[Pasted image 20250428234752.png]]

IO command
![[Pasted image 20250428235204.png]]

![[Pasted image 20250428235232.png]]

![[Pasted image 20250428235250.png]]
![[Pasted image 20250428235317.png]]

![[Pasted image 20250428235345.png]]

**Isolated vs Memory mapped IO**

	ISOLATED IO

![[Pasted image 20250429000249.png]]

the cpu places the address on the common address line and if its an IO instruction, it enables the IO read/write which informs the external components that the address on the common line is for an interface register and not for a memory word.

when cpu is fetching instruction from memory, it places the memory address on the address line and enables the memory read/write. this informs the external components that the address is for a a memory word and not for an IO interface.

![[Pasted image 20250429000600.png]]

	Memory Mapped IO

![[Pasted image 20250429000643.png]]

![[Pasted image 20250429000750.png]]
![[Pasted image 20250429000812.png]]

## Asynchronous Data Transfer

### Strobe and Handshaking

![[Pasted image 20250429002339.png]]

#### Strobe Control
![[Pasted image 20250429002708.png|400]]

the source places the data on the bus
the brief delay ensures that the data settles to a steady value
often the destination unit uses the falling edge of the strobe pulse to transfer contents of the data bus into one of its internal registers.

![[Pasted image 20250429002953.png|400]]
![[Pasted image 20250429003009.png]]
![[Pasted image 20250429003045.png]]

#### Handshaking

![[Pasted image 20250429003348.png]]

![[Pasted image 20250429003629.png|400]]
![[Pasted image 20250429003719.png]]

**Timeout**
![[Pasted image 20250429005101.png]]

### Asynchronous Serial Transfer

![[Pasted image 20250429005421.png]]
![[Pasted image 20250429005347.png]]
![[Pasted image 20250429005735.png]]

![[Pasted image 20250429005449.png]]

**Baud Rate**
![[Pasted image 20250429010141.png]]
![[Pasted image 20250429010147.png]]

#### Asynchronous Communication Interface

![[Pasted image 20250429010604.png|500]]

- it can act as both transmitter and receiver. mode of transfer can be selected through a control byte that is loaded onto the control register
- the transmitter register accepts data bytes from cpu through data bus. the byte is transferred into a shift register for serial transmission
- the receiver portion receives serial information into a shift register, and when complete data byte is accumulated, it is transferred to the receiver register. the cpu can select receiver register to read data byte through the data bus
- the bits in status registers are used for input and output flags for errors that may have occurred during the transmission.

![[Pasted image 20250429011117.png]]

	Working

![[Pasted image 20250429011218.png]]
![[Pasted image 20250429011232.png]]

### FIFO Buffer

	pending

# Modes of Transfer

![[Pasted image 20250429025256.png]]

	Programmed IO
data is typically transferred to and from cpu register and peripheral. 
the cpu constantly monitors the peripheral. once the data transfer is initiated the cpu monitors the interface to see when a transfer again can be made
problem - the cpu stays in program loop which is time consuming

	Interrupt initiated IO
the peripheral device issues and interrupt request signal to indicate when data is available from the device. the cpu can be executing any other program which is then interrupted and the cpu branches to a service program to process the io transfer and then returns to the task it was originally performing

	Direct Memory Access
the interface transfers data to/from the memory using the memory bus. the cpu only initiates the transfer by supplying the interface with the starting address and number of words needed to be transferred. the cpu merely delays its memory access operation to allow the direct memory io transfer.

![[Pasted image 20250429030855.png]]

##### Example of programmed IO

![[Pasted image 20250429031031.png]]
![[Pasted image 20250429030926.png|500]]
![[Pasted image 20250429031115.png|400]]

![[Pasted image 20250429032340.png]]

##### Interrupt Initiated IO
![[Pasted image 20250429033131.png]]
![[Pasted image 20250429033142.png]]

![[Pasted image 20250429033240.png]]
basically
non-vectored interrupt -> branch address is in a fixed location in memory
vectored interrupt -> the source provides the branch information called interrupt vector, can be direct/indirect address

# Priority Interrupt

![[Pasted image 20250429035518.png]]

![[Pasted image 20250429035955.png]]
![[Pasted image 20250507090338.png]]
disadvantage of polling
![[Pasted image 20250429040040.png]]

## Daisy Chaining

![[Pasted image 20250429040141.png]]

![[Pasted image 20250429040300.png]]
![[Pasted image 20250429040344.png]]
![[Pasted image 20250429040448.png]]

![[Pasted image 20250429040537.png]]
## Parallel Priority Interrupt

![[Pasted image 20250507091151.png]]
![[Pasted image 20250507091527.png]]

## Priority Encoder

![[Pasted image 20250507091502.png|500]]
![[Pasted image 20250507091611.png]]
![[Pasted image 20250507091642.png]]

## Interrupt Cycle

![[Pasted image 20250507091719.png]]
![[Pasted image 20250507091822.png]]
![[Pasted image 20250507091829.png|400]]
![[Pasted image 20250507091851.png|400]]
## Software Routines

![[Pasted image 20250507092828.png|550]]
![[Pasted image 20250507093032.png]]

## Initial and Final Operations
![[Pasted image 20250507093949.png]]

![[Pasted image 20250507094154.png]]
![[Pasted image 20250507094320.png]]
![[Pasted image 20250507094344.png]]
# Direct Memory Access

![[Pasted image 20250508043622.png]]
![[Pasted image 20250508043704.png]]
![[Pasted image 20250508043944.png]]
![[Pasted image 20250508043712.png]]

![[Pasted image 20250508043931.png]]
# IOP Processor

![[Pasted image 20250503063345.png|500]]

![[Pasted image 20250503063505.png]]
![[Pasted image 20250503063608.png]]

![[Pasted image 20250503063707.png]]

**CPU-IOP Communication**

Memory unit acts as a center where both processors leaves information for the other.

![[Pasted image 20250503064457.png]]

