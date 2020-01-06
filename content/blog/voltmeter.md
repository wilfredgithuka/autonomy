---
title: "Car Battery Dashboard Status Monitor"
date: 2020-01-06T07:53:59+03:00
draft: false
---

![display](/e11/multimeter.jpg)

So this weekend I have been busy adding more devices to the car.

For a while I have had the challenge of not knowing the status of the car battery
and wanted if there was a way I could get to know the voltage of the battery. I can connect
a multimeter but this is not convinient when driving.

My car has a normal Lead Acid Accumulator battery with a voltage of 12V at normal.
This value tends to range from +2V depending on wether its being charged or discharged.

When the atmospheric temperature drops, the battery current drops as well. In this case, 
the voltage is difficult to estimate, but it also slightly falls down, and if it is less than 
11.5V, then it indicates that the battery is discharged. In this case, the device 
will need an urgent charging, since its usage in such state will lead to the plate sulfation, 
which in turn will reduce the working capacity of the battery and the duration of its exploitation.

Nevertheless, if the voltage level hits below 11.6V, and the battery is almost completely discharged.

On fully charged the battery should have 12.6V and once the vehicle is turned on, this value should
flactutate between 13.7 to 14.7V

### Status

* 100% fully charged - 12.6V 

* 75% charged  - 12.4V

* 50% charged - 12.2V 

* 25% charged - 12.0V 

It can more than likely start the engine at a 50% charge an possibly at 25% charge, depending on the outside temperature and the condition of the engine.

To get an accurate reading of the battery voltage I got a [Digital Voltmeter Ammeter Dual Display 10A, 0-100VDC](https://store.nerokas.co.ke/index.php?route=product/product&product_id=1773). 

The specs for this small Voltimeter & Ammeter are as follows:

* Size: 48mm x 29mm x 21mm.

* Display color: Red & Blue LED (dual display).

* Display: 0.28" LED digital.

* Operating voltage: DC 4.5 ~ 30V.

* Measure voltage: DC 0 ~ 100V.

* Minimum resolution (V): 0.1V.

* Refresh rate: ≥500ms / times.

* Measure accuracy: 1% (± 1 digit).

* Minimum resolution (A): 0.01A.

* Operating Current: <20mA.

* Measure current: 10A (direct measurement, built-in shunt).

* Operating temperature: -10 to 65°c.

* Operating Humidity: 10 to 80% (non-condensing).

* Mounting cutout: 45.5mm x 26.5mm.

To get a voltage reading, connect the Yellow and Red wires together to the Battery + terminal. The B+ terminal can be accessed
from anywhere inside the car and it should represent the potential difference of the battery. Then connect the black to ground
of the car(car body). For the moment I can get the Voltage but not current. Current is much dependent on the load and I have
to find use for that.

I have mounted it just on the air-con ventilation panes and its readable during day and night. Due to the high brightness
of the diplay I was worried that It might drain the battery but on the second day the battery was good.

Overall its a good device to show the status of the battery.
