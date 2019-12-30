---
title: "Choosing A Good Microcontroller For The Car"
date: 2019-07-04T05:27:49Z
draft: false
---
Today is a good day for science.

Yesterday I stayed up late selecting which microcontroller I will use for the car project.

Well, its not that I had a plethora of chips to choose from, but on my workshop lay two chips:

* ATmega328
* STC15F2K60S2

### ATMega328

Lets first look at the ATmega328 is a single-chip microcontroller more closely. It has the following features:

* 8-bit RISC (Reduced Instruction Set Computer) processor core.
* Runs at clock speeds from 1MHz to 20MHz.
* 32Kb Flash Memory.
* 2Kb SRAM (Static Random Access Memory).
* 1Kb EEPROM (Electrically Erasable Read Only Memory).
* 23 GPIO (General Purpose Input-Output) lines.
* 32 general purpose registers.
* I2C, SPI, and Serial interfaces.
* 10-bit Analog to Digital converters – 6 in DIP package, 8 in surface-mount package.
* Internal and External Interrupts.
* Available in DIP and Surface Mount packages.

### STC15F2K60S2

The STC15F2K60S2 series MCU is a single-chip microcontroller based on a high performance 1T architecture
8051 CPU, which is produced by STC MCU Limited. It is a new generation of 8051 MCU of high speed, high
stability, low power consumption and super strong anti-disturbance. Besides, STC15F2K60S2 series MCU is a
MCU of super advanced encryption, because it adopts the eighth generation of STC encryption technology. With
the enhanced kernel, STC15F2K60S2 series MCU is faster than a traditional 8051 in executing instructions (about
8~12 times the rate of a traditional 8051 MCU), and has a fully compatible instruction set with traditional 8051
series microcontroller. This is what it packs under the Silicon:

![stc-image](/img/stc.png)

* 8-bit RISC Processor Chip
* Clock speeds: 5Mhz to 35Mhz
* 60kb Flash Memory
* 2Kb SRAM
* 1kb EEPROM
* 6 GPIO Registers
* SPI, UARTx2 and 2xSerial Interfaces(Independent).
* 10-bit Analogue to Digital Converters. 
* High speed 8-channels and 10-bits A/D Converter
* 8051 MCU with 1 clock per machine cycle
* High Speed and Reliability
* Super low power consumption, Very cheap
* Super Strong Anti-static electricity, Super Strong Anti-Disturbance

It seems that the STC15F2K60 scores highly against the ATMega328 but it lacking the I2C interface makes me
abit worried. Currently the Rpi connects to the Arduini via the I2C interface.

Also a challenge is that the many STC15F2K60 chips that I have all all surface mount chips. Converting this
to a breadboard so that I can access the pins well is another days work, but this is what am thinking of doing.

The STC15F2K60 seems more famous in China than outside so am sure apart from the [well documented](http://stcmicro.com/datasheet/STC15F2K60S2-en.pdf) data sheet,
I will be preety much on my own.

### stcgal

[Stcgal](https://github.com/grigorig/stcgal) is a command line flash programming tool for STC MCU Ltd. 8051 compatible microcontrollers. STC microcontrollers have an UART/USB based boot strap loader (BSL). It utilizes a packet-based protocol to flash the code memory and IAP memory over a serial link. This is referred to as in-system programming (ISP). The BSL is also used to configure various (fuse-like) device options. 

Unfortunately, this protocol is not publicly documented and STC only provide a (crude) Windows GUI application for programming.

In Linux to install stcgal do the following:

```
pip3 install stcgal
```
I would suggest not running this in a conda environment, since that has issues.

You can then call stcgal for options.
```
stcgal -h
```
### Supported MCU Models

stcgal should fully support STC 89/90/10/11/12/15/8 series MCUs.

So far, stcgal was tested with the following MCU models:

* STC89C52RC (BSL version: 4.3C/6.6C)
* STC90C52RC (BSL version: 4.3C)
* STC89C54RD+ (BSL version: 4.3C)
* STC12C2052 (BSL version: 5.8D)
* STC12C2052AD (BSL version: 5.8D)
* STC12C5608AD (BSL version: 6.0G)
* STC12C5A16S2 (BSL version: 6.2I)
* STC12C5A60S2 (BSL version: 6.2I/7.1I)
* STC11F02E (BSL version: 6.5K)
* STC10F04XE (BSL version: 6.5J)
* STC11F08XE (BSL version: 6.5M)
* STC12C5204AD (BSL version: 6.6H)
* STC15F104E (BSL version: 6.7Q)
* STC15F204EA (BSL version: 6.7R)
* STC15L104W (BSL version: 7.1.4Q)
* STC15F104W (BSL version: 7.1.4Q)
* IAP15F2K61S2 (BSL version: 7.1.4S)
* STC15L2K16S2 (BSL version: 7.2.4S)
* IAP15L2K61S2 (BSL version: 7.2.5S)
* STC15W408AS (BSL version: 7.2.4T)
* STC15W4K56S4 (BSL version: 7.3.4T, UART and USB mode)
* STC8A8K64S4A12 (BSL version: 7.3.9U)
* STC8F2K08S2 (BSL version: 7.3.10U)

Compatibility reports, both negative and positive, are welcome.

Next project >> Breakout board for the STCF2K60S2

Back to code...
