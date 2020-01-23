---
title: "Audio Unit Wiring Explained"
date: 2020-01-16T08:24:47+03:00
draft: false
---

After a whole week with no radio in my car, I have been busy trying to locate
the blown fuse for the audio unit. I suspect the problem could be far worse since
the side mirrors are no-longer working anymore.

I used the manual and therefore would recommend you first consult your users
manual before attempting any modifications to your car.

The Audio Unit is has 2 power inputs/outputs:

* Battery+ 12V
* ACC +12V
* GROUND

## Battery +12V

This wire is Light Green/Yellow in color and is connected to the vehicle's +12V terminal accross
a 15A Fuse Connection No:34. There is also present a 10A fuse before you reach the Audio
Unit using harness number: E101-M1. This 10A fuse is actually mounted on the radio itself.

The connection is as follows: BATTERY -> 15A FUSE -> 10A FUSE ->AUDIO UNIT

Note however that this +12V Line is connected directly from the battery through 2 virgin
control units *1A and *2B which have never been energised before on-board. This is the
same line which I hooked my voltimeter project.

The fuse for this line is located in the Fuseable link box right next to the battery. See the image below:

![fusable](/circuit/fuseable.jpg)

The cover for this fuseable link box has a map on which fuse controls what. Look at this carefully well.

## ACC +

This line is Blue and goes through Fuse Block(J/B) on M7 cable harness. The connection number is 16
and is protected by a 16A fuse. The connection point on the Audio unit is 37 but this might
change depending on the audio unit used.

From the battery the connection is as follows: BATTERY -> 80A FUSE -> ACC RELAY COIL -> 10A FUSE

Note that this 10A fuse is shared between the following devices:

* Ignition Key
* NATS - Nissan Antitheft System
* Mirrors
* Audio

This image below is the Fusebox which is located below the steering wheel.

![fusebox](/circuit/fuse_box.jpg)

Once again the cover for this fusebox shows a map of the fuses. I strongly suggest you read this
carefully before replacing the fuses.

Using a multimeter I noticed confirmed the fuses were indeed blown out and needed replacement. I also
tested the other fuses which were okay.

REMEMBER TO ALWAYS READ YOUR MANUAL
