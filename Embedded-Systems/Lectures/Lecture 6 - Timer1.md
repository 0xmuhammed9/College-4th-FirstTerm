---
Lecture-Date: 2024-11-24
Finish?: false
Study-Date: 2024-12-01
---
---
>[!Example] Main Topics
>-
>-
>

# Timer1 Registers 

- Is a 16-bit counter : TCNT1H, TCNT1L 

# Example 1 

>[!Question] (Example)
>write a micro-C program for ATmega16 MC to blink 8 LEDs connected to port B every 10 seconds. Use timer1 to time up the blinking process. Use interrupt mechanism. Assume the MC is running at clock rate of 1M Hz.

```c
void main(void){
DDRB=0xff;
PORTB=0xff;
SREG |=0x80;
TIMS |= (1<<OCIE1A);
OCR1A = 39061;
TCCR1A=0X00;
TCCR1B=0X0C;
}
void timer1_CTC_ISR(void) org 0x0c
{
PORTB = ~ PORTB;
}
```

![[TImer1Example1.webm]]


>[!Question] Example 2
> (Implementation of Digital frequency meter Using ATmega16 MC)A periodic signal with unknown frequency is applied to the input capture pin (ICP1) of timer1 of ATmega16 MC, write a micro-C program to measure the frequency of the applied signal.  Assume the frequency is a 16-bit number and it should be displayed on 16 LEDs connected to ports B and C.  Assume the MC is running at 1MHz.

```c
unsigned int startCount, endCount;
float deltaCount, timer1Freq;
unsigned int freq, pulseCountt;
unsigned short run;
void timer1_ICP1_ISR(void){{
if(run ==1){
if(puleseCount == 0)
	startCount=(ICR1H<<8)|(ICR1L);
else 
	endCount=(ICR1H<<8)|(ICR1L);
}
pulseCount+=1;
}}

void timer1_OVF_ISR(void){
run=0;
}
void main(void){
MCUCSR|=0X80;
DDRB=0XFF;
DDRC=0XFF;
SREG=|0X80;
TCCR1A=0X00;
TCCRB=0X02;
TIMSK|=(1<<TOIE1);
TIMSK|=(1<<TICIE1);
TCNT1=0;
while(1){
pulseCount=0;
run=1;
while(run==1);
deltaCount = (endCount - startCount);
timer1Freq=125000;
freq=(timer1Freq/deltaCount)*pulseCount;
PORTB=freq;
PORTC=(freq>>8);
}
}
```




