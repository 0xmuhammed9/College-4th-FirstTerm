---
Lecture-Date: 2024-10-23
Finish?: false
Study-Date:
---
---
>[!Example] Main Topics
>- Error Detection and Correction 
>	- Types of Errors
>	- Redundancy 
>- Data Link Control 
>	- Line Discipline 
>		- ENQ/ACK
>		- Poll/Select
>	- Flow Control 
>		- Stop and Wait
>		- Sliding Window
>	- Error Control 
>		- Stop and Wait ARQ 
>		- Sliding Window 
>			- Go back n 
>			- Selective reject

# Types of Errors 

-  Single 
	1. Only one bit changes 
	2. Caused by white noise 
	
![[Single.png]]

-  Multiple 
	1. Many bits changes at different times 
	
![[Multiple.png]]

-  Burst 
	1. Contiguous sequence of bits changes 
	2. Caused by impulse noise or by fading in wireless 
	3. Effect greater at higher data rates

![[Burst.png]]

![[TypesofErrors.webm]]



# Redundancy 

![[Redundancy.png]]


![[Redundancy.webm]]


---

# Line Discipline 


## 1. ENQ/ACK

- Two devices connected with dedicated link 
- Coordinate with device which may start transmission & whether or not recipient is ready & Enabled 


![[ENQ-ACK.mkv]]

## 2. Poll/Select

- Work where one device is Primary & others device is Secondary 
- Primary device control the link & and secondary device follow the instructions 
- Primary device determine which device will use channel & which time 
- Primary device initiator of session
- Primary device controls the link & it knows when link is available 
- Multipoint system guarantee only one transmission at a time because all control with primary device 


![[Poll-Select.mkv]]


# Flow Control 

## 1. Stop and Wait 

- Send one frame at a time 
- Source transmit frame --> Destination receive frame and reply with ACK 
- Source wait for ACK before sending the next frame
- Destination can stop flow by not send ACK 

![[stop-wait.mkv]]

## 2. Sliding Window 

- Allow multiple numbered frames to be transmit 
- RX has buffer space for W frames 
- TX sends up to W frame 

![[Sliding-Window.mkv]]



# Error Control 

- Detection and correction of errors
	- Lost frames 
	- Damaged frames 

## 1. Stop and Wait ARQ 

- Source transmits single frame --> Wait for ACK
- If received damaged frame 
	- Discard it 
	- Transmit has timeout 
	- If no ACK withing timeout, retransmit 
- If ACK damaged, transmitter will not recognize it
	- Transmitter will retransmit the last frame 
	- Receiver gets two copies of frame

![[stop-wait-arq.mkv]]


## 2. Go Back N ( Based on Sliding Window)

- if Not error, ACK as usual 
- Use window to control number of outstanding frames
- If error, reply with rejection
	- Discard that frame and all future frames until error frame received correctly 
	- Transmitter must go back and retransmit that frame and all subsequent frame 

![[gobackndamagedframe.mkv]]

![[gobackn-Cont.mkv]]


## 3. Selective Reject 

- Selective retransmission 
- Only rejected frames are retransmitted 
- Minimizes retransmission 
- More complex logic 

![[selectivereject.mkv]]

