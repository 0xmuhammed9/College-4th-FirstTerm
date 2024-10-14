___
  
>[!Question] Question 1
>An 8-bit input device (8 binary switches) is connected to port A of the AVR ATmega16
microcontroller and an 8-bit DAC is connected to port B. The output voltage of the DAC is driving a DC motor with sensitivity of 100 RPM/V. The binary number provided by the input device is to be used to control the speed of the DC motor through the 8-bit DAC.
(a) Write a micro-C program for ATmega16 MC to read the 8-bit data value provided by the input device every 3 seconds and apply it to the DAC to control the speed of the DC motor. Use timer0 as time base for this process.
(b) If the 8-bit data value applied by the input device is 7Fh, then what is the speed of the DC motor.

```c
main(void){
unsigned short var=0;
DDRA = ox00;
DDRB = oxff;
while(1){
var = PINA;
PORTB = var;
delay(3000);
}
}
```

>[!Question] Question 2
>Write a micro-C program for the Atmel AVR Atmega16 to display an incrementing binary
count on 8 LEDs connected to port B. The count should reset to zero when equal to the numberset on a bank of 8 switches connected to port A. The process should be in a for-ever loop.

```c
main(void){
unsigned short var =0;
unsigned short counter =0;
DDRA=0x00;
DDRB=0xff;
while(1){
PORTB = counter++;
var = PINA;
if(var>counter)
counter=0;
}
}
```
