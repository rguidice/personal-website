---
name: IR Smart Camera
date: 2019-10-16
tools: [Assembly, Python, Raspberry Pi, IR Sensor]
image: /assets/project_images/IR_Smart_Camera/project.JPG
blog: 1
sticky: true
github: https://github.com/rguidice/ir-smart-cam
description: Smart security camera built using an IR sensor, a Tiva TM4C123GH6PM Microcontroller, a USB webcam, and a Raspberry Pi.
---
# IR Smart Camera:

The purpose of this project was to take in IR sensor input from Tiva microcontroller and start recording video via a webcam controlled by a Raspberry Pi.

<p align="center">
	<img src="/assets/project_images/IR_Smart_Camera/project.JPG">
	<center> Project's main components (IR sensor not pictured). </center>
</p>

General Overview of Structure:

- IR sensor is 0/3.3V output connected to Port E on the Tiva microcontroller.
- Microcontroller is running Lab9.s, and uses a SysTick interrupt to check the first bit of Port E once per second. If it is a 1, it gets copied to Port B, the output port.
- The Raspberry Pi is connected to Port B on pin 35 and has IO.py running. IO.py constantly checks pin 35, and if it's high, will start recording via the attached webcam. It records for a pre-determined amount of time before checking if pin 35 is still high. If it is, it will continue recording, otherwise it will write the video and go back to polling pin 35.

Components used:

- Tiva Microcontroller (TM4C123GH6PM)
- Raspberry Pi 3B
- Creative Labs VF0415 Webcam
- [Gowoops HC-SR501 PIR Motion Sensor](http://osoyoo.com/2017/05/27/hc-sr501-pir-motion-sensor/)

Project written for Lab 9 of Colorado State University's ECE251 course, taught by Dr. Bill Eads.