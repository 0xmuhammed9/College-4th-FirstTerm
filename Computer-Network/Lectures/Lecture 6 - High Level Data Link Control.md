---
Lecture-Date: 
Finish?: false
Study-Date:
---
---
>[!Example] Main Topics
>-
>-
>

## Introduction to HDLC 
- High - Level Data Link Control : 
	- bit-oriented 
	- synchronous data link layer protocol.
	- Is the basis for many other important data link control protocols.

## Station Types
1. **Primary** : Control operation of Link
2. **Secondary** : Under control of Primary 
3. **Combined** : Issues command and responses.

## Link Configurations 
1. **Unbalanced** : 1 Primary - Multiple Secondary.
2. **Balanced** : Combined Stations.

![[Pasted image 20241112194911.png]]
![[Pasted image 20241112194929.png]]
![[Pasted image 20241112194939.png]]
![[2024-11-12 19-50-20.mkv]]


## HDCL Transfer Modes 
- Normal Response Mode (NRM)
	- Unbalanced Configuration 
	- Primary initiates transfer.
	- Used on Multi drop lines, eg (host +Terminals)
- Asynchronous Balanced Mode (ABM)
	- Balanced Configuration,
	- Either station initiates transmission 
	- Has no polling overhead, widely used.
- Asynchronous Response Mode (ARM)
	- Unbalanced configuration
	- Secondary may initiate transmit without permission from primary, rarely used.



# HDLC Frame Structure 

- Synchronous transmission of frames. 
- Single Frame format is Used .

![[Pasted image 20241112201146.png]]


## 1. Information Frames 

![[Pasted image 20241112202114.png]]

- This frame carry the data to be transmitted for the user.
- Flow and error control data (Contain sequence numbers to ensure frames are delivered in the correct order)
- Using the ARQ mechanism, are piggybacked on an information frame.

## 2. Supervisory Frames

![[Pasted image 20241112202517.png]]

- Used for flow control and error recovery.
- They don't contain user data and serve to manage the communication process.
- Provide the ARQ mechanism when piggybacking is not used.
- S-frames manage the data flow between devices and allow retransmission when errors are detected. 

![[Pasted image 20241112215053.png]]



## 3. Unnumbered Frames

![[Pasted image 20241112202729.png]]

- Manage the connection between devices.
- The are used for link establishment.
- Handle connection setup and management.
- They are essential for establishing and controlling the link between communicating devices. 

## HDLC Flag Field

![[Pasted image 20241112212711.png]]

- Bit stuffing used to avoid confusion with data containing flag seq.
	- 0 Insert after every sequence of five 1s
	- if receiver detects five 1s it checks next bit.
	- if next bit is 0, it is deleted (was stuffed bit)
	- if next bit is 1 and seventh bit is 0, accept as flag.
	- if sixth and seventh bit 1, sender is indicating abort.

## HDLC Address Field 

![[Pasted image 20241112214806.png]]


## Control Field 

![[Pasted image 20241112214831.png]]

- Different for different frame type.
- First 1-2 Bits of control field identify frame type.


