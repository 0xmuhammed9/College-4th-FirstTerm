---
Lecture-Date: 2024-10-08
Finish?: false
Study-Date: 2024-10-13
---
---
>[!Example] Main Topics
> - Programmable Parallel Input/Output Ports
> - Mechanisms of Interfacing the CPU with I/O 



>[!Summary]
>-
>-


# 1. Programmable Parallel Input/Output


## Structure of parallel input ports 

![[Structureofparallelinput.png]]

- Consists of 8  tristate buffers 

## Structure of parallel output ports 

![[strucureofparalleloutput.png]]

- Consists of 8-bit parallel in- parallel out register followed by 8 tristate buffers.

## Structure of parallel Input/output ports 

![[structureofinput-output.png]]


## Structure of programmable parallel Input/Output ports 

![[StructureofprogrammableparallelInputOutputports.png]]


>[!Question] Example 1
> Consider the AVR ATmega16 microcontroller circuit shown below. The circuit
has three switches S1, S2, and S3 which are connected to PA0, PA1, and PA2,
one push button (B1) which is connected to PA4, an alarm which is connected
to PB0 and a LED which is connected to PB4. This circuit should operate as
following: when one or more of the switches S1, S2, and S3 is ON, the alarm
should be activated, and the LED should be turned ON. When the button B1 is
pressed, the alarm should be deactivated, and the LED should be turned OFF.
Write a micro-C program for ATmega16 MC to operate this circuit.


![[Example1Lecture2.png]]

```c
Main(void)
{
short int x;
DDRA = 0x00; //set port A as input
DDRB = 0xFF; //set port B as output
PORTB = 0x00;
while(1)
{
x = PINA;
 //read port A
if ((x & 0x07) > 0x00)
{
PORTB = ox11;
}
if((x & 0x10) > 0x00)
{
PORTB = 0x00;
}
}
}
```

![[Example1Lecture2.mkv]]

