# Piboy-Pocket (WIP)

This project consists of a custom PCB that is designed to fit into an original Nintento Game Boy Pocket case. The PCB mates directly with a Raspberry Pi Zero and integrates all required functions into a single unit. Conductive button pads, LiPo charger, 5v Boost converter, USB audio codec, audio AMP, speaker output and headphone switch, volume pot, ATMEL microcontroller, and all external parts oriented to require minimal modifications to the case.

## Integrated Circuits used

Charger: MCP73871-2CCI
* Package: QFN-20
* Datasheet: http://www.mouser.com/ds/2/268/22090a-52174.pdf
* Functions: LiPo charger, load sharing, 3 status LED
* Cost: 10x $ (ea:$ )

Booster: MIC2876-5.0YMT
* Package: TDFN 8-pin
* Datasheet: http://www.mouser.com/ds/2/268/MIC2876-778590.pdf
* Function: 2MHz switching high efficiency(~95%) boost regulator, Enable pin, 5.0v out
* Cost: 10x $ (ea:$ )
    
MCU: ATMega16U2 (Still undecided, other choices include ATtiny88 32-pin, ATMega32U4, PIC16F570-I/SS)
  Package: QFN-32
  Datasheet: http://www.mouser.com/ds/2/36/doc7799-28769.pdf
  Functions: USB HID to Pi, 14 buttons, 4 analog
  Cost: 10x $19.20 (ea:$1.92)

AMP: PAM8403
* Package: MSOP-16
* [Datasheet](http://www.mouser.com/ds/2/115/PAM8302A-247351.pdf)
* Functions: Class-D 2.5w stereo speaker amp, Enable pin
* Cost: 10x $3.85 (ea:$0.385)
  
USB Codec:  PCM2704 (still deciding if needed)
* Package: SSOP-28
* Datasheet: http://www.mouser.com/ds/2/405/pcm2704c-485944.pdf
* Functions: USB Audio DAC
* Cost: 10x $21.22 (ea:$2.122)
  
USB Hub 4-port: FE1.1S
*  Package: SSOP28
*  [Datasheet](http://www.jfd-ic.com/Documents/FE1.1s%20Data%20Sheet%20%28Rev.%201.0%29.pdf)
*  [Example schematic](http://www.coldtears-electronics.com/images/FE1.1S.pdf]
*  Function: 1 upstream 4 downstream USB2.0 ports
*  Cost: 10x $5.15 ($0.515)

Micro JST 1.0mm 4-pin
  Cost: 30x $6.31 (ea:0.21)
  
Wifi Module: W12 RTL8188ETV USB
* Cost: 5x $12.11 (ea:$2.422)
* Basic useful feature list:

## Micro Controller functions

### Pinout

Currently a work in progress. Focusing in on the ATMega328 using the internal 8MHz oscillator and using V-USB to act as a HID device.

* 14 button inputs (14x digital)
* 1 analog joystick (2x analog)
* 1 Charger Enable (1 digital)
* 1 Pi shutdown (1 digital)
* 1 Power switch (1 digital)
* V-USB (TX/RX pins)/ or I2C ()

### Controller inputs
