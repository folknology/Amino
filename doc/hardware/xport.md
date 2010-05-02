---
layout: doc
title: Amino XPort Documentation
---

#Amino XPort Documentation

An Amino Xport is a peripheral extension interconnect to allow high bandwidth devices to dynamically connect into the Amino stack. An Xport provides up to 50MB/sec bandwidth via a nibble (4 bit) based interface. The nibble interface is implementedt using a 2 row 0.1" header with the 4 bit signals on row 1 and 4 pins of supply and GND on the second row. An additional 4 x 1 bit biderectional control pins are provided adjacent to the 4 bit bus allowing flexible transfer and multiplexing schemes depending on application. Alternatively the entire connector can be used as 8 bidirectional bits in any matter appropriate to the peripheral. The pinout of a connector is shown below:

|1.P1|  |2.P0|

|3.P3|  |4.P2|

|5.+V|  |6.P3.3|

|7.+V|  |8.P3.2|

|9.GND| |10.P3.1|

|11.GND| |12.P3.0|

|13.XCK| |14.XDA|




