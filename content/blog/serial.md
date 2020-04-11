---
title: "BigBox Serial Attempt 2"
date: 2020-04-11T21:37:13+03:00
draft: false
---
This is the second attempt with little to no success at reading the serial output of 
an old Safaricom Big Box.

![top](/carputer/top_pins.JPG)

When I run screen, the following is the output:

```
Uncompressing Linux ... done, booting the kernel
```
The above statement is the output when I run the following command

```
sudo screen /dev/ttyUSB0
```

[Screen](https://www.gnu.org/software/screen/) or as it is known GNUScreen is a full-screen window manager 
that multiplexes a physical terminal between several processes. 

I am a member of [uucp group](https://wiki.archlinux.org/index.php/Users_and_groups#User_groups)which 
gives me priviledges to use RS-232 serial ports and devices connected to them.

### Hardware Setup

As with the previous setup at using a cheap USB TTL Serial Adapter. The PIN out is as follows:

* Red --> 5V
* Green --> Transmission Tx
* White --> Receive Rx
* Black --> GND

The images shows this clearly.

![no-red](/carputer/top_pins_no_red.JPG)

![below](/carputer/reverse_pins.JPG)

If you can solve this issue please send me an email.

I will come back to this project on another day, am sure there is a way to solve this.

Thanks for reading :-)

## References

* [Medium-Reverse Engineering To Gain Shell](https://medium.com/@shubhamgolam10/reverse-engineering-uart-to-gain-shell-de9019ae427a)
* [devttyS0](http://www.devttys0.com/2012/11/reverse-engineering-serial-ports/)
* [serialport-GPS](http://www.python-exemplary.com/drucken.php?inhalt_mitte=raspi/en/serial.inc.php)
