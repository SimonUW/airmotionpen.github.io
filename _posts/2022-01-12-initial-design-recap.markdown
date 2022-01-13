---
layout: post
title:  "Initial Design Recap"
date:   2022-01-12 22:52:00 -0500
categories: design
---

# Background

The AirMotion Pen was designed to explore the use of peripheral devices to develop a user-friendly device that functions on a variety of platforms while incorporating the functionalities of optical mice and digital pens. The goal of the AirMotion Pen is to create a portable peripheral device that serves as both a mouse and a stylus pen on multiple platforms including desktops, laptops and tablets and can provide smooth user experience for switching between the cursor control and writing functionality.

## Initial Design

The initial chosen design includes a combination of hardware and software components.The movement of user’s hand is the input of the device which is captured by the motion sensor MPU6500. A Teensy 4.1 controller is used to manipulate the data collected by the motion sensor and the pressure sensor MPM281 to allow the device to read the data of 2048 pressure levels and ±90 degrees of inclination angles and can perform all the tasks a regular stylus can perform. To allow the device to perform cursor control tasks like a mouse and capture the users gesture, an algorithm is developed to model the motion of the stylus and continuously track the pen tip’s position in 3D spaces. In addition, a Sensel board can be used as an optional add on element to enhance the accuracy of pressure readings of the hand to track hand movements. 

![airMotionPenInitDesign.png](/assets/images/airMotionPenInitDesign.png)

## Next Steps

The next steps to be done are:
- Collect more data for the prototype model from other participants
- Obtain a gesture recognition model and check Teensy functionality for running models
- Search for more available components and verify compatibility
- Develop the project webpage and research ptoentail prizes
- Connect components and get readings
- Implement all functionalities
  - Convert MPU readings to local screen coordinates 