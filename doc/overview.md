---
layout: doc
title: Amino Software Architecture Overview
---

#Amino Software Architecture (ASA)#

The Amino stack is built in 3 distict layers:

1. Layer 1 - Hardware Service Modules
2. Layer 2 - Management and Communications
3. Layer 3 - Application and Sketches

##Hardware Service Modules - [HSM](hsm.html)##

Layer 1 is designed to enable hardware modules to be written which interface directly to the I/O pins and event based model. Modules need to comply to a basic interface enabling them to be loaded, configured, managed and finally unloaded freeing up any resources used. We are aiming to keep such template code to a minimum and get out of your way, but given the shared nature of the modules running at this level some basic lifecycle management is beneficial to all modules. The Ethernet module is itself an example of a HSM, as is any other of the included hardware modules. Code for this layer is written in XC (and perhaps C) and debugged onboard using and Alpha card, no other hardware is required.

##Managment and Communications - [MC](mc.html)##

Layer 2 is dedicated to managing the Amino board and its HSMs along with communications services TCP/IP, USB, serial and I2C (Later we may be adding Canbus/Canopen and others). It also manages iternal SPI peripherals including flash, MicroSd cards, co-processors such as alpha's analogue and comms co-pro. Some boards such as Alpha have built in management HSMs for monitoring, debugging testing layer 1 HSMs. This layer effectively manages resources and board operation along with providing external communications.

##Applications and Sketches - [AS](as.html)##

Layer 3 is the most abstracted layer and is where participants can create running applications and or sketches. Most applications will be written using XC abd will lean heavily on Amino libraries/modules above abstracting layes 1 and 2. These applications are written and externally debugged (using Xtag/Xtag2) via the XIDE from Xmos. Sketches will be written in Amino third party languages. Atb this time what those languages are is still being determined, we expect several candidates to emerge and become popular. We also envisage these sketches being created and operated via a web front end, more information will follow on this later.


