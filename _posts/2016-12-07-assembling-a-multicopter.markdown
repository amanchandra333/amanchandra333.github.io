---
title: "Assembling a Multicopter"
layout: post
date: 2016-12-07 02:37
image: /assets/blog/IMG_20160905_230423.jpg
headerImage: true
tag:
- multicopter
- quadcopter
- robotics
blog: true
star: false
author: amanchandra333
description: Assembling a quadcopter with a low level flight controller
---
Beep Beep Beep Whirr! And the mechanical bird soared up and away! Indeed, **Aerial Robotics** is the most intriguing field in the world of Robotics.

## Summary
<div class="breaker"></div>

This blog is a guide to assemble a multicopter with an onboard low level microcontroller, starting from the very quad-root level.
Hop onboard, let's get started.



## Configuration
<div class="breaker"></div>


### APM/Pixhawk - *The Low Level Controller*:


![APM](/assets/blog/apm.jpg)

Ardupilot Mega (APM) is an IMU autopilot that is based on the Arduino Mega platform. It is capable for autonomous stabilisation, way-point based navigation and two way telemetry with Xbee wireless modules, supporting 8 RC channels with 4 serial ports.  ArduPilot Mega consists of the main processor board and the IMU shield which fits above or below it.

### Motors and ESCs:
![Motor and ESC](/assets/blog/motor1.jpg)
The copter uses 850kV *brushless DC motors*, each with a dedicated Electronic Speed Controller of current rating 40A. The ESCs provide electronically generated three-phase electric power low voltage source of energy for the motor. The PPM signal for the control comes from the APM. ESCs can be BEC or OPTO.




