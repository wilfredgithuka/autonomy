---
title: "Time To Get Moving — My First Autonomous Car Project"
date: 2017-04-20T08:24:12Z
draft: false
---

The Python study program is over, am so excited to get my hands working on something. Last year I got a Red Hammer H2 RC Car. This car is made in China 1:14 and runs on 5x1.5V .I want to learn how to make it drive itself. Am sure there are tutorials online but I wanna make my own version . Currently it is controlled by a remote and has good suspension kits installed. When I got this car last year, I was excited to start tinkering about self driving cars but was stopped on my heels due to not having Python skills, which I have now :-). So lets gets moving.

The first thing I need to do is to reconfigure the remote control. It transmits at 27MHz to the car which is bad since it is really affected alot by walls. The 27MHz is for low cost cheap RC cars. More expensive RCs operate upto 2.4 GHz. Yes I know how crazy that sounds. The problem with the 27Mhz is that if the remote gets lost, another remote wont work for my RC car. That’s how bad the situation is.The remote also features a 9V battery to power it. I dismantled the remote, got the circuit board, analysed it and mounted in on bread board so that I could access the button controls.


![Circuit board mounted on a bread board](/car1/circuit.jpeg)

After following the circuit layout I concluded that the buttons are fed into a TX-2B CMOS LSI which is responsible for the button controls and transmission to the car. In the car there is another TX-2B for the receiver. I break out the board onto the breadboard, rewire the buttons and also provide them with a direct connection onto the breadboard. Power from the 9V batter is first fed onto the breadboard power bus then tapped into the circuit board. Now I can control the car from the breadboard.

![RC Car Batter pack](/car1/power.jpeg)

The power for the RC is supplied by the above China made low cost batters which I used for testing phase only. They cost Ksh.20 (USD 0.2) each. They can spit out good power but don’t last for long.

![Testing….OK](/car1/h2.jpeg)

After the soldering and modding, the car responded to my modifications well. The next work is to connect the modded remote set to an arduino and write some Python code. Cant wait :-)

Thanks for reading.
