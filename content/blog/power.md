---
title: "Fundamentals of A Dual Battery Power System"
date: 2020-04-05T08:56:07+03:00
draft: flase
---
For a while I have been designing components to be added to my Nissan Note but over
time I have realised one problem.Power

All these devices need to be connected to the car battery and the last thing I want
is to have a dead/low battery unable to crank the engine. So I need a way to isolate/protect
the car battery from overusage when the engine is not running.

In a dual battery setup, there are two battery units in the car, the starting battery and the
second usage battery. The starting battery is for starting the engine and while the engine
is running, it charges both battery units. When the engine is OFF, there is an isolator which
connects the load to the second battery. In some connections, the secondary battery can also
help the main starting battery should it be too low. This is however beyond the scope of this manual.

## My Setup

* Primary Battery - Wet Lead Acid Battery 12V
* Secondary Battery - Sealed Lead Acid Battery 12V 7.0AH


### Primary Battery

This is a common old car starting battery 12V which is at its glory days. I think its time I replaced
this unit but time will tell. It works well but on cold days it can fall to 9V which is normaly a hit and
miss situation if it can start the engine. I have installed a voltmeter to monitor its state. You can 
read about it here. In a dual battery setup which am planning to design, this battery will remain as it is
and it shall be used only for starting the car.

### Secondary/Aux Battery

This is new 12V 7.0 AH PK1270 Sealed Lead Acid Battery.

#### Composition

* Negative Electrode: Lead (Pb)
* Positive Electrode: Lead Dioxide (PBO2)
* Electrolyte: Dilute Sulphuric Acid (H2SO4)
* Battery Shell: ABS Plastic
* Separator: Glass Fibre (Silicon Dioxide)
* Terminal: Silver Coated Copper

#### Discharging

The battery is rated at 7.0AH(Ampere Hours). This means that you can draw A Amps for 7 hours straight before it
gets drained flat. from the formula of charge, Q=IT  ie Charge(C) = Current(I) X Time (Hours), we can also say

* 0.35 Amps (350 mAH) for 20 Hours
* 0.5 Amps (500 mAH) for 14 Hours
* 1 Amps for 7 Hours
* 2 Amps for 3.5 Hours
* 3 Amps for 2.3 Hours
* 4 Amps for 1.7 Hours

From the above epressions, we can see that as the current drawn increases, the duration decreases.

#### Charging

This sealed lead acid battery contains 6 cells inside it so when charging one has to be very careful not to overcharge
them since this will eventually destroy them. According to the manuafacturer the recomended charging  voltage is 14.20-15V
with a current less than 2.10A. From [LahisTech's Youtube Video](https://www.youtube.com/watch?v=-0RAHOAd50Y) I have found a way to charge this battery from the car's alternator while the engine is running.

The car alternator has an output of 13.5V when the engine is running which is sufficient to charge, but what I need to
take car of is the charging current which should be best at 0.7A-0.8A. I need to use a [DC-DC Buck Converter](https://www.ebay.com/itm/5A-DC-DC-Step-Down-Buck-Converter-Module-Power-Supply-LED-Lithium-Charger-XL4015/182391151322?hash=item2a775c1ada:m:mabZ7S_ZBKjDtlkxKBv1KHQ) which has
a variable current adjustment.

### Excpected Loads and Their Rating

* RaspberryPi: 0.5-1A without wifi and camera
* Wifi Router: 1.5-2A
* Voltimter: 0.2A

Thats it for now, let me embark on designing the charging circuit then I shall update asap. Remember to take care when working with batteries.
