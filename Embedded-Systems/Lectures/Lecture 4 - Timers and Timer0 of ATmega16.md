---
Lecture-Date: 2024-10-27
Finish?: true
Study-Date: 2024-11-02
---
 ---
>[!Example] Main Topics
>-
>-
>


___

- Timers used to compute time and perform other functions such as generating pulse-width modulation waveforms.

## The Block diagram of an N-Bit Timer

![[Pasted image 20241101031938.png]]

## Structure of Prescaler (10-bit Prescaler)

![[Pasted image 20241101032953.png]]

- 10-bit Prescaler is made up of 10-bit counter and 8x1 multiplexer.
- The counter is to generate output waveforms with different frequencies and the multiplexer is to select the output waveform with required frequency.
## Output Waveform of the Prescaler 

![[Pasted image 20241101141325.png]]

## Structure of Timer0 of ATmega 16 Microcontroller 

![[Pasted image 20241101141447.png]]

## Structure of Timer0 With its control and status registers

![[Pasted image 20241101141609.png]]


## Clock selection of timer0

![[Pasted image 20241101141846.png]]

## Registers of Timer0

![[Pasted image 20241101141910.png]]

## Modes of Operation for Timer0

![[Pasted image 20241101141937.png]]



- Main Registers 
	-  Timer/Counter Control Register - TCCR0 : 
		- CS00, CS01, CS02 : Select the clock source to be used by the Timer/Counter
	- Timer/Counter Register - TCNT0 : 
		- اعتقد دا الى بيبدأ يعد 
	- Output Compare Register - OCR0 : 
		- Contains an 8-Bit Value that is continuously compared with the counter value (TCNT0)
	- Timer/Counter Interrupt Mask Register - TIMSK 
		- OCIE0-Bit : Interrupt bit of Output Compare Match 
		- TOIE0-Bit : Interrupt bit of Timer/Counter overflow 
	- Timer/Counter Interrupt Flag Register - TIFR :
		- OCF0-Bit :  Set When the Data on OCR0 Compare to the TCNT0
		- TOV0-Bit : Set when an overflow occurs in TCNT0


![[Pasted image 20241102103555.png]]



>[!Question ] Midterm Question 
>


