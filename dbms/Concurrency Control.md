![[Pasted image 20250513223225.png]]

# Time stamp ordering protocol

• With each transaction ti , in the system, we associate a unique fixed timestamp, denoted by TS(ti).
• This timestamp is assigned by database system to a transaction at time transaction enters into the system.
• If a transaction has been assigned a timestamp TS(ti ) and a new transaction tj , enters into the system with a timestamp TS(tj ), then always TS(ti) < TS(tj).

![[Pasted image 20250513223404.png]]

![[Pasted image 20250513223415.png]]

![[Pasted image 20250513223434.png]]
![[Pasted image 20250513223445.png]]

Thomas Write Rule
![[Pasted image 20250513224051.png]]
![[Pasted image 20250513224628.png]]

# Lock based protocols

![[Pasted image 20250513224929.png]]
![[Pasted image 20250513224938.png]]

![[Pasted image 20250514163620.png]]
![[Pasted image 20250514163629.png]]
![[Pasted image 20250514163635.png]]
![[Pasted image 20250514163743.png]]
![[Pasted image 20250514163759.png]]

![[Pasted image 20250514163818.png]]
![[Pasted image 20250514163901.png]]

![[Pasted image 20250514163938.png]]
![[Pasted image 20250514163946.png]]

![[Pasted image 20250514163953.png]]
![[Pasted image 20250514164000.png]]
![[Pasted image 20250514164006.png]]

![[Pasted image 20250514164013.png]]

![[Pasted image 20250514164445.png]]
rigorous 2pl can have deadlocks

![[Pasted image 20250514164704.png]]

deadlock prevention
![[Pasted image 20250514165035.png]]
![[Pasted image 20250514165041.png]]

![[Pasted image 20250514170136.png]]
![[Pasted image 20250514170143.png]]

![[Pasted image 20250514170233.png]]
![[Pasted image 20250514170328.png]]
T1: tries → backs off → tries again → ...
T2: tries → backs off → tries again → ...

![[Pasted image 20250514170342.png]]
![[Pasted image 20250514170414.png]]
![[Pasted image 20250514170424.png]]
