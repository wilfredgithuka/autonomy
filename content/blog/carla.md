---
title: "CARLA Release 0.96 on Archlinux"
date: 2019-08-19T13:33:03Z
draft: false
---
![carla](http://carla.org/img/posts/2019-07-12/pedestrians.gif)

CARLA is an open source simulator for autonomous driving research.

Its the kind of tool that AI and Autonomous Driving techies can use
to speed up research in a real world simulation environment.

Carla has been in development for a while now and mid last year
I tried to install in on my Arch machine, it was tough.

Carla was built on Ubuntu and best runs on Ubuntu, but I dont use Ubuntu.

With this new release however, its more simpler to run it on Archlinux. This release brings back long-requested features, such as automatic pedestrian navigation (AI-controlled), better visual quality and a new skeleton control API, among other improvements.

Just follow the steps below:

* Update your machine

```
pacman -Syu
```
* Activate your Python Conda environment
```
conda activate deeplearning
```
* Update your Conda evironment(if necessary)
```
conda update --all
```
* Downgrade to Python 3.5.6 You will thank me later.
```
conda install python=3.5
```
* Download [Carla zip](http://carla-assets-internal.s3.amazonaws.com/Releases/Linux/CARLA_0.9.6.tar.gz). Its 2.9GB
* Extract
* Install required files for Carla through python's pip
```
pip install carla future pygame
```
* The examples shall be stored in the PythonAPI folder. You can check there to confirm
* Run ./CarlaUE4.sh to load the simulator. It shall run but without any cars or peds
* Minimise that and in the PythonAPI folder run:
```
python spawn_npc.py -n 900
```
* This will spawn over 900 cars. You can work with a lower value.

Success :-)

The guys over at Carla have made an amazing [documentation](https://carla.readthedocs.io/en/latest/), you can always consult it.
