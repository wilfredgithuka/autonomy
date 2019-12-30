---
title: "Vehicle Android Tablet Heads Up Display and Media Center"
date: 2019-12-28T19:11:28+03:00
draft: false
---

The internet is awash with so many in-car head up displays from so many manufaturers.

Lets face it the stock HUDs are so boring and old school, not apealing at all.

In this project I mnaged to fit an old Android Tablet in replacement of my car audio
to also play music and display data from the ECU.

The data from the ECU is transmitted via a [Bluetooth OBD2 device](https://www.jumia.co.ke/generic-car-diagnostic-tool-mini-auto-scanner-elm-327-bluetooth-for-android-torque-obdii-v1.5-vehicle-scan-16220519.html).

The current setup looks like below:

![done-image](/e11/music.jpg)

## Step1: Modification of Old Audio System

My current setup is not at all a replacement of the old radio, infact its more
of an upgrade. The Android table is meerly an audio source and by no means 
can it be able to send an audio signal to the vehicle's speakers alone.

![radio](/e11/old_radio.jpg)

I needed an amplifier. Thats where the old radio came in.

I connected the jack pin from the tablet to the aux in of the car radio and it worked.

Thats basically the priciple of operation.

## Step2: Mounting of the Android Tablet.

The Android tablet which am using is a preety old one, made by Lenovo in 2013. The tablet
needs to sit in the front panel and luckily it fits sunggly since its has 7 inches of screen size.

![final](/e11/final.jpg)

But for the tablet to fit well, the radio had to either be removed or stashed back inside since
I dont operate it anymore. I chose the latter.

I carefully unmounted it from the mounts and brackets, then carefully tilted it to standing position 
inside the radio compartment. To my suprise there is alot of space inside there. 

![radio-position](/e11/radio_inside.jpg)

For the tablet to work well, it needed two things:

* Power Connection
* Audio Signal

I removed the front panel and worked on it in my lab to ensure that the tablet was mounted correctly.

The USB Power Connection goes inside the dash and come put below which I connect to the USB cigarette lighter. The Audio signal cable also run inside
and connects to the old radio's aux port.

## Software & Apps

On the Android Tablet I had to make the following settings to increase visiblity and easier, safer operation during driving.

### Apps

* [F-Droid](https://f-droid.org/en/)  - Install open source apps on the go
* [Volume Control](https://play.google.com/store/apps/details?id=netroken.android.persistfree&hl=en) - Control volume on screen since volume keys are unaccessible
* [AndrOBD](https://f-droid.org/en/packages/com.fr3ts0n.ecu.gui.androbd/) - Connects with the OBD2 bluetooth device to show data.

### Settings

* Enable developer mode.
* Increase text size to max.
* Add useful apps to home screen.
* Allow screen to move to landcape mode.
* Remove unwanted apps to make it work faster.
* Set Standby time to 2 mins.

## Driving Experience

The Driving expereince this week has been good and I have learnt alot especially when it comes to safety, the following is a summary of how
the week was with this new setup.

#### Pros

* Good Audio, Video & Podcasts selection of my favourite tracks.
* Easy operation.
* Great aesthetics and looks cool
* EDGE Internet connection(Requires SIM card)

#### Cons

* Table can get warm when the car is parked in the sun
* During midday tablet screen can barely be seen due to sun's glare
* OBD2 Data can be slow to respond especially the revmeters.

## Recomendations

I need a much faster app which will read data from the OBD2 and diplay it well. I tend to think its a bluetooth issue but am not
ready to spend cash to buy a cable. Also the old radio sitting inside gives me jitters. Am thinking of a way I can extend its wires
and send it to the back of the car or below the seats. 

Remember to read the car's owners manual before attempting this project and Keep Your Eyes on The Road.
