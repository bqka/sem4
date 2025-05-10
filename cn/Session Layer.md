![[Pasted image 20250421020110.png]]

![[Pasted image 20250421020439.png]]

## ****Functions of Session Layer****

The session layer performs several different as well as important functions that are needed for establishing as well as maintaining a safe and secure connection:

1. ****Session Establishment**** : It establishes and manages sessions between communicating parties that cab be connection-oriented or connectionless. It also maps sessions to transport connections.
2. ****Communication Synchronization**** : It ensures reliable connectivity and recovery by using ****synchronization bits**** and ****checkpoints**** in data stream.
3. ****Activity Management**** : It allow the user to divide data into logical units called activities. An activity can be processed on its own and each activity is independent of activities that come before and after it.
4. ****Dialog Management**** : It refers to deciding whose turn it is to talk. Some applications uses a ****token mechanism**** for half-duplex mode, where only one party holds the token to transmit data while other supports full-duplex mode for simultaneous data transmission.
5. ****Data Transfer :**** It manages data exchange between systems.
6. ****Resynchronization :**** In this,  all the tokens are restored to the positions that were set during synchronization. The various options for resynchronization includes set, abandon and restart.

## ****Working of Session Layer****

- The Session Layer manages communication sessions between applications over a network.
- It establishes connections, negotiating session parameters like authentication and communication direction (full-duplex or half-duplex).
- It oversees data exchange by using tokens to manage transmission rights and prevent collisions.
- Synchronization techniques are implemented, inserting checkpoints for recovery in case of disruptions.
- It ensures orderly communication, reducing message loss, duplication, or errors caused by overlapping communication.
- The Session Layer gracefully terminates the session, ensuring all data is exchanged and both sides agree to close

# RPC

![[Pasted image 20250510055435.png]]
![[Pasted image 20250510055447.png]]
![[Pasted image 20250510055639.png]]
![[Pasted image 20250510055719.png]]
