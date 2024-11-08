---
Lecture-Date: 2024-10-09
Finish?: true
Study-Date: 2024-10-19
---
---
>[!Example] Main Topics
>- Line Configuration 
>- Topology 
>- Transmission Mode 
>- Categories of Networks 
>- Internetworks 




# Network Topologies 

- Physical
	- Describes how devices are physically cabled 
- Logical 
	- Describes how devices communicate across physical topology 


## Mesh Topology 

![[MeshTopology.png]]

- Provide protection from interruption of service 
![[MeshTopologty.webm]]
![[MeshTopologyEnhance.webm]]
- Each host has its own connections to all others hosts
- The Reliability is very high (100%) because if one link is fail there is another link to the device
- Very high cost 
- <span style="color:rgb(0, 176, 80)">Used in </span>
	- Systems that have many numbers of users 
	- Data is sensitive and must transmit to the destination 



## Bus Topology 

![[Bus.png]]

- Use a single backbone cable that is terminated at both ends.
- All the hosts connect directly to this backbone. 
- One host send data ---> Data move through the buss and reaches all the other hosts.
![[BUs.webm]]

## Star Topology 

![[Star.png]]

![[Star.webm]]
- Best type and the most used 


## Ring Topology 

![[Ring.png]]

- Connect one host to the next and last host to the first.
- Creates a physical ring of cable 
- If the first host needs to send data to the last host, the data must path through all the hosts before reaching the end host .

![[Ring.webm]]

# Types of Computer Network 


## A. Based on Size 

1. PAN 
	- Covers range 10 meters 
	- personal devices (smartphones, tablets, laptops)
1. LAN
	- group of network components that work within small area  
2. MAN
	- Group of LANs that are interconnected withing small area 
3. WAN
	- Group of LANs that are interconnected within large area


## B. Based on Scope 

1. Intranet
	- Private network that used internet to facilitate communication  within an organization
2. Extranet 
	- Extranet extends an intranet to include external parties such as customers, suppliers, or partners 
3. Internet
	- Global network

## C. Based on Ownership

1. Private 
2. Public 

## D. Bases on Technology 

1. Switched 
	- Used devices such as switches or routers to forward data packets
2. Broadcast 
	- Transmit data packets to all devices 
	- allowing each device to receive and process the information
3. Point to Point 
	- Direct connection between two devices 
	- enable communication without the need for intermediate devices 

## E. Based on Protocol 

1. TCP/IP 
2. IPX/SPX
3. Apple Talk