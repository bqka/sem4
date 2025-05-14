![[Pasted image 20250512193117.png]]
![[Pasted image 20250512193156.png]]
![[Pasted image 20250512193210.png]]
![[Pasted image 20250512193219.png]]
![[Pasted image 20250512193230.png]]
![[Pasted image 20250512193237.png]]

![[Pasted image 20250512193300.png]]
![[Pasted image 20250512193349.png]]
![[Pasted image 20250512193356.png]]
![[Pasted image 20250512193417.png]]
![[Pasted image 20250512193423.png]]
![[Pasted image 20250512193433.png]]

![[Pasted image 20250513220619.png]]

![[Pasted image 20250513220658.png]]

PROBLEMS DUE TO CONCURRENT EXECUTION OF TRANSACTION 
• But interleaving of instructions between transactions may also lead to many problems that can lead to inconsistent database. 
• Sometimes it is possible that even though individual transaction are satisfying the acid properties even though the final statues of the system will be inconsistent.

When two or more transaction executed together or one after another then they can be bundled up into a higher unit of execution called **schedule**.

**Serial schedule** - A serial schedule consists of sequence of instruction belonging to different transactions, where instructions belonging to one single transaction appear together. Before complete execution of one transaction another transaction cannot be started. Every serial schedule lead database into consistent state.

**Non-serial schedule** - A schedule in which sequence of instructions of a transaction appear in the same order as they appear in individual transaction but the instructions may be interleaved with the instructions of different transactions i.e. concurrent execution of transactions takes place.

**Conflict equivalent** – if one schedule can be converted to another schedule by swapping of non- conflicting instruction then they are called conflict equivalent schedule.

the instructions I and J are said to be conflicting, if they are operations by different transactions on the same data item, and at least one of these instructions is a write operation.

![[Pasted image 20250513221110.png]]
![[Pasted image 20250513222431.png]]

![[Pasted image 20250513221128.png]]

![[Pasted image 20250513221250.png]]

![[Pasted image 20250513221338.png]]
![[Pasted image 20250513221347.png]]

A schedule S is view serializable, if it is view equivalent to a serial schedule

![[Pasted image 20250513221513.png|350]]

1. **Non-Recoverable Schedule**:  
    A schedule is **non-recoverable** if there exists a pair of transactions **Ti** and **Tj** such that **Tj reads a data item written by Ti**, and **Tj commits before Ti commits or aborts**. This can lead to inconsistency if **Ti later aborts**, because **Tj has committed based on unconfirmed (dirty) data**.
    
2. **Recoverable Schedule**:  
    A schedule is **recoverable** if for every pair of transactions **Ti** and **Tj**, where **Tj reads a data item previously written by Ti**, the **commit of Ti occurs before the commit of Tj**. This ensures that **if Ti aborts**, **Tj can also be aborted**, maintaining the correctness of the database.
    
3. **Cascadeless Schedule**:  
    A schedule is **cascadeless** if, for every pair of transactions **Ti** and **Tj**, whenever **Tj reads a data item written by Ti**, the **commit of Ti occurs before the read operation by Tj**. This ensures that **no transaction reads uncommitted (dirty) data**, thus avoiding cascading rollbacks.
    
4. **Strict Schedule**:  
    A schedule is **strict** if a transaction can **neither read nor write** a data item **until the last transaction that wrote to it has committed or aborted**. This ensures both **recoverability** and **cascadelessness**, providing the highest level of safety.
![[Pasted image 20250513222317.png]]
S2 and S3 are strict schedules

![[Pasted image 20250513222338.png]]

![[Pasted image 20250513222403.png]]

![[Pasted image 20250514163526.png]]
![[Pasted image 20250514163533.png]]
