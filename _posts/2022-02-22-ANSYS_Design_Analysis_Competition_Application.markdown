---
layout: post
title:  "ANSYS_Design_Analysis_Competition_Application"
date:   2022-02-22 13:00:00 -0500
categories: design
---

# Focus
Verification of design using computational or numerical analysis using appropriate engineering tools (eg. CFD, FEA, statistical)

# Requirement
![ANSYS_requirement.PNG](/assets/images/ANSYS_requirement.PNG)

# Project Overview

## Summary of Analyses
- Gesture recognition model
  - Collect hand gesture motions for 7 different gestures -> 10 sets each's
  - 70 data samples per person for 3 people (210 total)
  - Data splitting -> training set and test set 80/20%
  - TPTN (true positive, true negative)
  - Test cases -> measure overall
- Multithreaded system
  - Reliability
- Take out sensel

## Analysis Procedures (award)
1. We measured the data transmission rate between the microcontroller and the PC end through the Bluetooth protocol. A low transmission rate will affect the gesture recognition accuracy, so a high rate is desired. We also measured the stability of the Bluetooth connection and the optimum transmission should be stable for hours without loss in data.
  - Bluetooth 2.0 communication protocol
  - C++ = driver of digital stylus
    - running in driver program - measuring
  - data transmission rate = 280 Hertz 
  - data transmission was stable without loss of data within an hour of running
  - processing time of each sample of data could match the 280 Hertz
    - data was processed synchronously





