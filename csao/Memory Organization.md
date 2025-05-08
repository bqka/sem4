![[Pasted image 20250503092445.png|500]]

![[Pasted image 20250503092559.png]]

Static and dynamic RAM
![[Pasted image 20250503092807.png]]

ROM
![[Pasted image 20250503093500.png]]

![[Pasted image 20250503093530.png]]

## RAM and ROM Chips

![[Pasted image 20250503093926.png|500]]
![[Pasted image 20250503094248.png]]

![[Pasted image 20250503094324.png|500]]

## Memory Address Map
![[Pasted image 20250503094707.png]]

![[Pasted image 20250503094727.png]]
Refer book page 451

## Memory Connection to CPU

![[Pasted image 20250503095051.png]]
![[Pasted image 20250503095103.png]]

![[Pasted image 20250503095143.png]]

# Auxiliary Memory

--pending--

# Associative Memory

![[Pasted image 20250503095412.png]]

## Hardware Organization
![[Pasted image 20250503095446.png|400]]
![[Pasted image 20250503095619.png]]

![[Pasted image 20250503100148.png|500]]
![[Pasted image 20250503100225.png|400]]

Match Logic => ![[Pasted image 20250503100450.png|250]]

![[Pasted image 20250503101029.png|400]]

Read Operation
![[Pasted image 20250503101100.png]]

Write Operation
![[Pasted image 20250503101153.png]]
![[Pasted image 20250503101235.png]]

# Cache Memory

Locality of reference
![[Pasted image 20250503101512.png]]

hit ratio
![[Pasted image 20250503101754.png]]

![[Pasted image 20250503102500.png]]

![[Pasted image 20250503132050.png|400]]

in below examples,
main memory has 32k words of 12 bits
cache memory has 512 words of 12 bits

main memory requires 15 bits which are stored in 5 bit octal
cache requires 9 bit which are stored in 3 bit octal
## Associative mapping

like a hashmap

![[Pasted image 20250503130644.png|400]]
![[Pasted image 20250503130707.png]]
![[Pasted image 20250503130721.png]]
## Direct mapping

![[Pasted image 20250503131517.png]]

![[Pasted image 20250503131355.png]]
![[Pasted image 20250503131403.png]]
![[Pasted image 20250503131417.png]]

this example uses block size of 1 word, for block size of 8 words, consider the following

![[Pasted image 20250503131444.png|500]]
![[Pasted image 20250503132404.png]]

**Disadvantage of Direct Mapping**
![[Pasted image 20250503132444.png]]
## Set Associative mapping

![[Pasted image 20250503132619.png]]
![[Pasted image 20250503132544.png|400]]
![[Pasted image 20250503133604.png]]
![[Pasted image 20250503133616.png]]

![[Pasted image 20250503133635.png]]

## Writing into cache

Write through and write back

![[Pasted image 20250503134027.png]]

## Cache initialization

![[Pasted image 20250503134535.png]]

# Virtual Memory

![[Pasted image 20250503135110.png]]

## Address Space and Memory Space

![[Pasted image 20250503135148.png]]

![[Pasted image 20250503142156.png]]
![[Pasted image 20250503142628.png]]
![[Pasted image 20250503142647.png]]

![[Pasted image 20250503142657.png]]

## Address matching using pages

![[Pasted image 20250507064008.png]]

![[Pasted image 20250507064129.png]]
![[Pasted image 20250507064144.png]]

![[Pasted image 20250507064201.png]]
![[Pasted image 20250507064425.png]]

## Associative Memory Page Table

![[Pasted image 20250507064547.png]]

![[Pasted image 20250507064627.png|450]]
![[Pasted image 20250507064715.png]]
![[Pasted image 20250507064732.png]]

hash map jesa

## Page Replacement

![[Pasted image 20250507064928.png]]

page fault
![[Pasted image 20250507064946.png]]

page fault -> execution of program suspends -> loading a page from auxiliary to main memory is i/o operation -> OS assigns this to I/O processor -> control transferred to next program -> when page transferred, program continues

FIFO
![[Pasted image 20250507065202.png]]

LRU
![[Pasted image 20250507065252.png]]