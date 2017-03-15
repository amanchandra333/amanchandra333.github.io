---
title: "Noida Workshop"
layout: post
date: 2017-03-15 02:37
image: /assets/blog/head1.jpg
headerImage: true
tag:
- robotics
- workshop
blog: false
star: false
author: amanchandra333
description: Robotix Workshop at Bennett University, Noida.

---
Beep Beep Beep Whirr! And the mechanical bird soared up and away! Indeed, **Aerial Robotics** is the most intriguing field in the world of Robotics.

## Summary
This blog is a guide to assemble a multicopter with an onboard low level microcontroller, starting from the very quad-root level.
Hop onboard, let's get started!

---

## In this blog

- [APM/Pixhawk - *The Low Level Controller*](#apm)
- [Motors and ESCs](#motors-and-escs)
- [LiPo - *The Power Source*](#the-power-source)
- [RC Transmitter and Reciever](#rc-transmitter-and-reciever)
- [GPS](#gps)
- [Assembly](#assembly)
- [Motor Order Diagrams](#motor-order-diagram)
- [Attaching Propellers](#attaching-propellers)
- [Mission Planner](#mission-planner)
- [Loading Firmware](#loading-firmware)
- [Compass Calibration](#compass-calibration)
- [Radio Control Calibration](#radio-control-calibration)
- [Accelerometer Calibration](#accelerometer-calibration)
- [ESC Calibration](#esc-calibration)
- [Flight Modes](#flight-modes)
- [Arming the Motors](#arming-the-motors)
- [Fly!](#fly)
- [What's next?](#the-high-level-microcontroller)

---


## APM

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/apm.jpg" alt="Alt Text">
        <figcaption class="caption">The APM Flight Controller</figcaption>
    </div>

    <div class="toright">
        <p>Ardupilot Mega (APM) is an IMU autopilot that is based on the Arduino Mega platform. It is capable for autonomous stabilisation, way-point based navigation and two way telemetry with Xbee wireless modules, supporting 8 RC channels with 4 serial ports.  ArduPilot Mega consists of the main processor board and the IMU shield which fits above or below it.</p>
    </div>
</div>

---
