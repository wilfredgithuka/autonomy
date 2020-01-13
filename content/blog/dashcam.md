---
title: "Raspberry Pi+Webcam Based Dashcam"
date: 2020-01-10T09:06:53+03:00
draft: false
---

Its time for my car to have eyes. It needs to see the road ahead.

One of the main cimponents of a connected autonomous vehicle is the
ability to percieve its environment. This is made possible by sensors
and cameras. This is the main difference between Waymo and Tesla.

I have a Raspberry Pi which I plan to connect a desktop USB webcam to
it providing the crucial vision function.

## Hardware
* Raspberry Pi
* USB Webcam

## Software
* FFmpeg
* mpv
* OpenSSH
* Python

## Connectivity
* Serial
* Wifi
* USB
* LAN RJ45

## Setting Up The Raspberry Pi

On the Raspberry Pi I will be running [Archlinux ARM](https://archlinuxarm.org/forum/index.php?sid=063f51be110fbd0238a9280f9253795b). After installation
be sure to update your system:

```
sudo pacman -Syu
```
Install required software & tools

```
sudo pacman -S ffmpeg mpv openssh python
```
Next install software for the USB Webcam

```
sudo pacman -S v4l-utils mpv xawtv
```
The Raspberrypi shall be running headless thats why I installed openSSH. Once that is done, its time to connect the hardware.

## USB Camera Setup

Connect the USB Webcam and list USB Devices.

```
sudo lsusb
```
The device should be listed, if not I would suggest reading the [Archlinux Wiki](https://wiki.archlinux.org/index.php/Webcam_setup) about webcam support.
Most recent webcams are UVC (USB Video Class) compliant and are supported by the generic uvcvideo kernel driver module. To check that your webcam is recognized, run dmesg just after you plug the webcam in.

```
dmesg | tail
```
Once this is complete, its time to take some photos and videos.

Since I will be using C to write programs to the Pi inorder to access the camera, some setup has to be done.


