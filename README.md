##\*uino-1284p 

\*uino-1284p is an Arduino compatible platform based on the Atmel ATmega1284P-AU microcontroller.

###Licensing

This work is licensed under a Creative Commons Attribution-ShareAlike 3.0 Unported License, CC BY-SA.

You are free to copy, distribute and transmit the work. You must attribute the work in the manner specified by the author or licensor (but not in any way that suggests that they endorse you or your use of the work). you alter, transform, or build upon this work, you may distribute the resulting work only under the same or similar license to this one.  

Please refer to [http://creativecommons.org/licenses/by-sa/3.0/] for the license.

###Credit

The *uino-1284p is derived from previous work done by:

- The Arduino team <http://arduino.cc/>

###Details

The *uino-1284p board utilizes the ATmega1284P microcontroller. The main goal of this project is to be able to access more memory, both FLASH and RAM, while keeping the Arduino UNO compatible board size and I/O assignments.

The ATmega1284P provides 128k of FLASH and 16k of RAM. It has 10 more I/O pins then the ATmega328P. The additional I/O pins are brought out to a 5x2 header in a non-standard Arduino position. The extra header pins are :

        L1/D16  o|o  L2/D17
           D18  o|o  D19
           D20  o|o  D21
           D22  o|o  D23
        D24/A6  o|o  D25/A7


The design features a dedicated ATmega8U2 for USB connectivity. The circuit has been taken from the Arduino UNO but the TQFP-32 package was chosen for easy solderability.

Power supply input for the board is selected via a jumper. Power supply options are USB bus powered or unregulated DC input. An onboard LDO regulator will accept an unregulated input voltage between 6.4V and 15V.

###Arduino

The board is supported in Arduino IDE 1.6.x via the core files available at: [https://github.com/adilinden/uino-arduino]

To install clone uino-arduino into the hardware folder inside your Sketchbook folder. The board will then automagically appear in the Boards menu.

###Pin Mapping

```
*uino     ATmega1284p                     Function
A0  D26   32 - PA5 (PCINT5/ADC5)
A1  D27   33 - PA4 (PCINT4/ADC4)
A2  D28   34 - PA3 (PCINT3/ADC3)
A3  D29   35 - PA2 (PCINT2/ADC2)
A4  D30   36 - PA1 (PCINT1/ADC1)
A5  D31   37 - PA0 (PCINT0/ADC0)

D0        9  - PD0 (PCINT24/RXD0/T3)      UART RX0
D1        10 - PD1 (PCINT25/TXD0)         UART TX0
D2        11 - PD2 (PCINT26/RXD1/INT0)    IRQ2, UART RX1
D3        12 - PD3 (PCINT27/TXD1/INT1)    IRQ3, UART TX1
D4        13 - PD4 (PCINT28/XCK1/OC1B)    PWM
D5        14 - PD5 (PCINT29/OC1A)         PWM
D6        15 - PD6 (PCINT30/OC2B/ICP)     PWM
D7        16 - PD7 (PCINT31/OC2A)         PWM

D8        42 - PB2 (PCINT10/INT2/AIN0)  
D9        43 - PB3 (PCINT11/OC0A/AIN1)    PWM
D10       44 - PB4 (PCINT12/OC0B/SS)      PWM, SPI SS
D11       1  - PB5 (PCINT13/ICP3/MOSI)    SPI MOSI
D12       2  - PB6 (PCINT14/OC3A/MISO)    PWM, SPI MISO
D13       3  - PB7 (PCINT15/OC3B/SCK)     PWM, SPI SCK, LED

SCL D14   19 - PC0 (PCINT16/SCL)          SCL
SDA D15   20 - PC1 (PCINT17/SDA)          SDA
L1  D16   21 - PC2 (PCINT18/TCK)          L1
L2  D17   22 - PC3 (PCINT19/TMS)          L2

D18       23 - PC4 (PCINT20/TDO)
D19       24 - PC5 (PCINT21/TDI)
D20       25 - PC6 (PCINT22/TOSC1)
D21       26 - PC7 (PCINT23/TOSC2)
D22       40 - PB0 (PCINT8/T0/XCK0)
D23       41 - PB1 (PCINT9/T1/CLK0)
A6  D24   30 - PA7 (PCINT7/ADC7)
A7  D25   31 - PA6 (PCINT6/ADC6)
```

