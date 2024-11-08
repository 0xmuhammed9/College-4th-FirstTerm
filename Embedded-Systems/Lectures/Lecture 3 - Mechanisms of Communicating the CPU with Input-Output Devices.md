---
Lecture-Date: 2024-10-13
Finish?: true
Study-Date: 2024-10-27
---
---
>[!Example] Main Topics
> - Introduction 
> - Pooling Mechanism 
> - Interrupt Mechanism 
> 	- Types of Interrupt 
> 	- Interrupt Examples 
> 	- Interrupt Processing 
> 	- Managing Interrupts, Masking 
> - Interrupt System of ATmega16
> - Interrupt Execution 
> - Problelms

# Introduction 

- Each device must have a means of indicating its status of the CPU (Input/Output)
- There are two common mechanisms for managing communications between the CPU
	- Polling Mechanism 
	- Interrupt Mechanism 

# Polling Mechanism 

- Allow the CPU to determine the status of an I/O device 
- CPU Regularly pools the I/O device to determine the device's status.
- Requires that the CPU regularly asks the input/output devices what is happening.
- <span style="color:rgb(0, 176, 80)">Examples</span> : 
	- Is an error Condition being Occurred ?  
	- Is a switch being thrown?
	- Is the data from the device ready? 
	- Is the device ready to receive the data? 

### Flow Chart 

![[Pasted image 20241028101712.png]]

-  Advantages : 
	- Software is straightforward 
- Disadvantages :
	- Interact with device even when no service is needed
	- Response time can be long 
# Interrupt Mechanism 

- Allows a device to get the attention of the CPU
- The operation of the interrupt:
	- Interrupt signal are hooked to the CPU.
	- When signal asserted and interrupts are enabled --> CPU is interrupted.
	- CPU stops doing what is was doing and jumps to an ISR  --> Execute ISR.
	- When ISR is done, the CPU resumes the task it was doing before the interrupt.

## Types of Interrupts 

- External device 
- Internal device 
- Illegal instruction or memory access (Exception)
- Special Instruction (Traps)

## Interrupt Processing 

![[Pasted image 20241028103557.png]]

![[Pasted image 20241028103628.png]]

- Interrupt mechanism is structured as follows: 
	- The peripheral device interrupt the processor 
	- Current instruction execution is completed 
	- The address of the next instruction is sored on the stack
	- Address of the ISR are loaded into the program counter. It also turns of the interrupt system to prevent further interrupts while one is in progress.
	- The processor executes the ISR 
	- The ISR execution completion is indicated by the RETI instruction ( return form the interrupt).
	- The processor loads the program counter with the value stored on the stack and normal program executions resumes
	- The processor status (flags, etc.) must be saved so that normal program execution can resume after the ISR is completed. 

![[Pasted image 20241028105108.png]]
![[Interrupt.mkv]]



> [!Question] Problem 4
>  Draw a diagram to show how an interrupt request is executed.

![[Pasted image 20241028110729.png]]
![[Problem4.mkv]]


