---
layout: post
title:  "Component Consideration"
date:   2022-01-28 13:00:00 -0500
categories: design
---

## Using an external battery supply for the Teensy board 4.1
Currently, we have the prototype powered by a USB cable that connects to the Teensy board 4.1. To switch to an external battery, additional configurations are required. For the purpose of prototyping, we want to have both the USB cable and external battery as possible sources. Considering that both power supplies could be connected at once, we want to avoid draining the battery when the USB is connected. Should we decide to only use one power source, it is still recommended to configure the board to protect it from accidental reverse polarity connections. 
The configuration suggested by [PJRC](https://www.pjrc.com/teensy/external_power.html) is to cut apart the "5V" pads and connect two 1N5817 diodes. The first diode should be connected between the cut apart pads with the cathode facing the center pad. The second diode should be connected between the Teensy board's Vcc(+5V) pin and the battery.
The following notes should be be considered for the battery configuration with the Teensy 4.1:
* A voltage above 5.5 V will cause the Teensy to start browning out
* A voltage below 3.6 V will result in the Teensy to shut down
* If the battery setup supplies a voltage below 5.5 V and above 3.6 V, a buck boost regulator should be considered to improve the power efficiency
* If the battery setup supplies a voltage above 5.5 V, a linear regulator or a buck converter should be considered to improve the power efficiency

## Thoughts on the IMU approach
1. The AHRS algorithm performs poorly on our MPU in terms of calculating Euler angles, there are heavy drifts and it’s much worse than the XIO’s demo. So if we want to accurately model the rotational motion, we could purchase the XIO NGIMU. But the NGIMU won’t help us model the translational motion with its linear acceleration measurement.
2. The IMU could provide accurate Euler angles to control cursor coordinate, but modeling the translational motion is impossible. At best, we can get linear acceleration without gravity, a translational motion consists of both accelerating and decelerating motions, so the motions will cancel out in terms of distance. So the best approach would be to use LED transmission like a normal mouse or only support in-air control, which will be accurate for daily usage.
3. In general, the NGIMU definitely provides really accurate measurements that the current IMU could not reach. It’s worth buying if we want accurate rotational measurements.
