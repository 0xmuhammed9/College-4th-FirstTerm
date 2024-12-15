---
Lecture-Date: 2024-11-27
Finish?: false
Study-Date: 2024-12-04
---
---
>[!Example] Main Topics
>-
>-
>

# Introduction 

- LANs serve as the backbone of communication within organizations, institutions, and even homes.

## Definition and Purpose 

- Refer to networks that connect computers and devices within a limited area (single building)
- They facilitate resource sharing, data transfer, and communication among devices connected to the network.

# LAN Architecture

## LAN Topologies 

- Topology refers the the way in which the end points, or stations, attached to the network are interconnected. (Ring, Start, Bus and so)


## LAN Components 

- Network Interface Cards (NICs)
- Switches 
- Routers
- Access Points 
- Cables 
- Network Protocols 


# LAN Protocols 

![[lanprotocols.png]]

## IEEE 802 Layers (1)

- Physical Layer
	- Encoding/Decoding of signals 
	- Preamble generation/Removal 
	- Bit transmission/Reception 
	- Transmission medium and topology 

## IEEE 802 Layers (2)

- Logical Link Control 
	- Interface to higher levels.
	- Flow and error control. 
	- Media Access Control.
	- On transmit assemble data into frame.

## MAC Frame

![[macframe.png]]

## PDU Format 

![[pduformat.png]]

# ALOHA 

- Is a system for coordinating and arbitrating access to a shared Communication Networks Channel. 
- There are two different types
### Pure ALOHA
- Developed for packet radio networks.
- Station may transmit a frame at any time
- If frame is determined invalid, it is ignored.
- Maximum Utilization of channel about 18%.
![[purealoha.png]]
### Slotted ALOHA
- Organized slots equal to transmission time.
- Increased utilization to about 37%
![[slotedaloha.png]]

