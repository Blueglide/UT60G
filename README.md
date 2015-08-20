# UT60G

This repository describes hardware and software required to support a RS-232 connection between the popular Sinometer UT60G Digital Multimeter and an Arduino UNO microcontroller. 

The UT60G DMM is available from sources like Amazon.com for around $40.00. It is built around the Cyrustek <a href="http://www.cyrustek.com.tw/spec/ES51978.pdf">ES51978</a> chip for which the data sheet appears to be correct in most but NOT ALL respects. However I believe all inaccuracies have been identified and corrected in the software provided here. 

Three RS-232 connections between the UT60G and a microcontroller such as the Arduino UNO are required. (Rx, DTR, and Gnd). Additionally a means must be provided to translate between the TTL logic voltage levels of the microcontroller and RS-232 logic levels of the UT60G interface. A simple schematic of a suitable level conversion circuit for this using the popular MAX232 chip is provided as a pdf file in this repository.

Although the UT60G is capable of continually sending a new data packet related to the current meter reading out its RS-232 port about once per second, the DTR handshake line and related software provided here will only query the Digital Multimeter and receive a response data packet when requested by the Arduino sketch. 

Note that due to the optical isolation provided by the UT60G RS-232 interface, NO electrical connection exists between the meter and the Arduino microcontroller.


