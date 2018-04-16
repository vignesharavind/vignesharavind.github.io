---
slideinit: >-
  <section markdown="1"
  data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section
  markdown="1">
vertical: </section><section markdown="1">
horizontal: >-
  </section></section><section markdown="1"
  data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section
  markdown="1">
layout: post
title: Automatic Pick and Place Robot for Palletizing
author: Vignesh
tags: Design Solidworks Arduino Automation
subtitle: 3-DOF Robotic Arm
category: project
published: true
visualworkflow: true
---
<!-- Start Writing Below in Markdown -->

<section markdown="1" data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section markdown="1">
## {{ page.title }}

<hr>

#### {{ page.author }}

#### {{ page.date | date: "%I %M %p ,%a, %b %d %Y"}}


## Overview

3-AXES PICK AND PLACE ROBOTIC ARM is a project that is aimed at designing a robotic arm with less number of axes by applying kinematic principles to create joints and constrains restricting the motion to three degrees of freedom. The three degrees of freedom allows the robot to move all through its work envelope. Servo motors are used as actuators to control different links of the arm. 3-axes robotic arm could be useful for domestic and industrial applications like welding, painting, assembly, pick and place, product inspection and testing. Usually a standard 6 axis robots are used in the industries for many applications because of its greater reliability and versatility. These robots provide cost effective solutions and can perform pick and place operations in risky and hazardous environment.

The proposed prototype is controlled using AVR’s advanced ATmega328p microcontroller which is programmed using Arduino software in C program language. The end effector used in this prototype is a mechanical gripper which is actuated by servo motor and the bell crank lever mechanism is used for opening and closing of the claws. This project forms a good platform for robotics and helps budding engineers understand the real-world problems and domestic automation needs. The problem with the available arms are that they cost quite a deal of money and hence not affordable to plebeians. Most of the robotic arms available are bulky and robust thus, can’t be used to do household chores. The objective of this project is to design a compact and cheap robotic arm to serve this purpose.

![Robotic arm with link](/img/app/robotic-arm-link.png)
<p align="center">Robotic arm with links</p>

![Bell crank mechanism](/img/app/bell-crank-mechanism.png)
<p align="center">Gripper with 'bell crank mechanism'</p>

![Exploded View.jpg]({{site.baseurl}}/img/Exploded View.jpg)
<p align="center">Exploded view of robotic arm</p>

## Fabrication

The material chosen is cut into various links as required. After cutting the links and base to suitable dimensions they are subjected to required machining processes. Holes are drilled in base to accommodate DC Motor and a flange like entity is made to connect arm’s base with the DC Motor. The links are then attached to the base using L-clamps, screws and bolts with the aid of washer.Servomotors of suitable dimensions are also attached to the respective links. 
![Fabrication_1](/img/Pick-Place/Pic_6.jpg)
<p align="center">Base of Robotic Arm</p>

![Fabrication_1](/img/Pick-Place/Pic_7.jpg)
<p align="center">Links of Robotic Arm</p>

The electrical circuit of the robot is as follows:
![Electrical Circuit](/img/app/electrical-circuit.png)


The designed gripper mechanism was stimulated using Adams software
![Fabrication_1](/img/Pick-Place/Pic_8.jpg)

![Fabrication_1](/img/Pick-Place/Pic_9.jpg)

The gripper used in the robotic arm is the bell crank lever mechanism which is very different from conventional grippers that use gears to achieve the gripping action.
