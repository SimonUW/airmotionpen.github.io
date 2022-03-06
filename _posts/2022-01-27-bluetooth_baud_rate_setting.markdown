---
layout: post
title:  "Change the Baud Rate of HC-06 Bluetooth Module"
date:   2022-01-27 22:00:00 -0500
categories: design
---

# Instruction and Example

The bluetooth connection requires the bluetooth module, serial port, and laptop all have the same baud rate. Otherwise, the laptop is not able to read anything through the bluetooth. In case of changing the baud rate of our bluetooth module ”HC-06”, the first thing to do is cutting all connected devices so that the module can run under AT-mode. After that, we initialize a ‘SoftwareSerial’ object which takes the pin number of RXD and TXD as its parameters. In the setup function, we begin the new defined ‘SoftwareSerial’ object using the current baud rate on the bluetooth module. Then, we use the ‘SoftwareSerial.write()’ function to send an AT command to the bluetooth module. The command “AT+BAUDi” is used to set a new baud rate, where 1=1200, 2=2400, 3=4800, 4=9600, 5=19200, 6=38400, 7=57600, 8=115200, and the data type of the command must be character string. The figure below is an example of changing the baud rate from 9600 to 115200.


![changeFrom9600To115200.PNG](/assets/images/changeFrom9600To115200.PNG)
