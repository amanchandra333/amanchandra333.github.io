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
This blog is a guide to assemble a multicopter with an onboard low level microcontroller, starting from the very quad-root level.
Hop onboard, let's get started.

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

## Motors and ESCs

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/motor1.jpg" alt="Alt Text">
        <figcaption class="caption">BLDC Motor and ESC</figcaption>
    </div>

    <div class="toright">
        <p>The copter uses 850kV Brushless DC Motors, each with a dedicated Electronic Speed Controller of current rating 40A. The ESCs provide electronically generated three-phase electric power low voltage source of energy for the motor. The PPM signal for the control comes from the APM. ESCs can be BEC or OPTO.</p>
    </div>
</div>

---

## The Power Source

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/tattu.jpg" alt="Alt Text">
        <figcaption class="caption">LiPo Battery</figcaption>
    </div>

    <div class="toright">
        <p>A Lithium Polymer battery of rating 11.1V, 3s, 5000mAh, 20C is used for powering the motors. The battery provides an average flight time of 8-10 minutes.</p>
    </div>
</div>

---

## RC Transmitter and Reciever

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/rc.jpg" alt="Alt Text">
        <figcaption class="caption">6 Channel Reciever and Transmitter</figcaption>
    </div>

    <div class="toright">
        <p>The quadcopter is controlled by a 6 channel 2.4 GHz RC transmitter and a 6 channel PPM receiver in manual mode. The bandwidth of the transmitter is 500Hz.</p>
    </div>
</div>

----

## GPS 

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/gps.jpg" alt="Alt Text">
        <figcaption class="caption">Ublox Neo-M8N GPS module</figcaption>
    </div>

    <div class="toright">
        <p>The Ublox Neo-M8N GPS module includes a HMC5883L digital compass.It outputs precise position updates at 10Hz. The Ublox NEO-M8N is configured to run at a baud rate of 38400. </p>
    </div>
</div>

---

## Assembly

The illustration below highlights a typical installation of a quadcopter. It contains optional equipment including a Camera, Gimbal and a Battery Monitor and it utilizes an ESC wired "Y" power connection rather than the power distribution board common to many MultiCopters.

![Assembly](/assets/blog/assembly.jpg)

---

### Motor Order Diagram

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/order.jpg" alt="Alt Text">
        <figcaption class="caption">Motor Order for Quad X</figcaption>
    </div>

    <div class="toright">
        <p>The figure shows motor order for Quad X (the numbers indicates the connected autopilot output pin) and the propeller direction (clockwise (CW) motors are shown in green and take pusher propellers,counterclockwise motors (CCW) are shown in blue and take puller propellers. Diagrams for other frames can be found on the official <a href="http://ardupilot.org/copter/docs/connect-escs-and-motors.html">Arducopter Website</a></p>
    </div>
</div>

---

### Attaching Propellers


<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/prop.jpg" alt="Alt Text">
        <figcaption class="caption">Recognizing clockwise and counterclockwise propellers</figcaption>
    </div>

    <div class="toright">
        <p>The diagrams shows two types of propellers: clockwise (called pushers) and counterclockwise (called pullers). It is most reliable to recognize the correct propeller type by its shape as shown below. Note that the propellers below have the edge with the shallow consistent curve at the leading edge in direction of rotation and the more radical scalloped (and usually thinner edge) as the trailing edge.</p>
    </div>
</div>

---

## Mission Planner

Mission Planner is free, open source software available for Windows. The latest version can be downloaded from [here](http://firmware.ardupilot.org/Tools/MissionPlanner/MissionPlanner-latest.msi).

---

### Loading Firmware

Once you’ve installed the Mission Planner onto your computer, connect the autopilot board to your computer using the micro USB cable. Windows should automatically detect and install the correct driver software.

Open the Mission Planner and select the COM port drop-down on the upper-right corner of the screen (near the **Connect** button). Select **AUTO** or the specific port for your board (**PX4 FMU** or **Arduino Mega 2560**). Set the Baud rate to **115200** as shown. Don’t hit **Connect** just yet.

On the Mission Planner’s **Initial Setup->Install Firmware** screen select the appropriate icon that matches your frame (i.e. Quad, Hexa). Answer **Yes** when it asks you “Are you sure?”.

If all goes well you will see some status appear on the bottom right including the words, “erase...”, “program...”, “verify..” and “Upload Done”. The firmware has been succesfully uploaded to the board.

![Install firmware](/assets/blog/firmware.jpg)
<figcaption class="caption">Mission Planner: Install Firmware Screen</figcaption>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://amanchandra333.github.io/website/assets/blog/port.jpg" alt="Alt Text">
        <figcaption class="caption"></figcaption>
    </div>

    <div class="toright">
        <p>Select the desired port and data rate and then press the Connect button to connect to the autopilot. After connecting Mission Planner will download parameters from the autopilot and the button will change to Disconnect as shown.</p>
    </div>
</div>

---

## Compass Calibration

* Under Initial Setup->Mandatory Hardware select Compass.


![Install firmware](/assets/blog/compass.jpg)
<figcaption class="caption">Mission Planner: Live Compass Calibration</figcaption>



