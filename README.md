Welcome
==========
This is a Beaglebone port of the popular RF24(nrf24l01) library posted on https://github.com/maniacbug/RF24/. 
If you find the library is out of sync with the Arduino library please drop an email to purinda@gmail.com 

Copyright (C) 2011 James Coliz, Jr. <maniacbug@ymail.com>
Copyright (C) 2012 Purinda Gunasekara. <purinda@gmail.com>
Contains portions of the GPIO library posted here,
https://github.com/mrshu/GPIOlib 

Complete wiki can be found here 
http://maniacbug.github.com/RF24Network/index.html 

Features
==========
Refer to RF24 documentation.
http://maniacbug.github.io/RF24/index.html

Requirements
==============
You need a beaglebone with SPI enabled. Look here for a tutorial http://www.yellowfeather.co.uk/2012/03/userland-spi-on-the-beaglebone-with-ubuntu/

How to connect the pins
I used one of these boards to test the library. http://imall.iteadstudio.com/media/wysiwyg/Products/IM120606002_nRF24L01module/RF24013.jpg

- Connect PIN 1 (GND) of NRF24L01 board to Expansion header P9 PIN 1(GND) of Beagleboard
- Connect PIN 2 (VCC) of NRF24L01 board to Expansion header P9 PIN 3(3v3) of Beagleboard
- Connect PIN 3 (CE) of NRF24L01 board to Expansion header P9 PIN 27(GPIO3_19) of Beagleboard
- Connect PIN 4 (CSN) of NRF24L01 board to Expansion header P9 PIN 27(GPIO3_21) of Beagleboard
- Connect PIN 5 (SCK) of NRF24L01 board to Expansion header P9 PIN 31(SPI1_SCLK) of Beagleboard
- Connect PIN 6 (MOSI) of NRF24L01 board to Expansion header P9 PIN 30(SPI1_D1) of Beagleboard
- Connect PIN 7 (MISO) of NRF24L01 board to Expansion header P9 PIN 29(SPI1_D0) of Beagleboard

Notes
======

Note that the library uses a GPIO pin in BeagleBone as CS pin, which is an workaround/issue exist in the code. Planning to fix it whenever I have time.

Project is written using NetBeans and I have commited some files used by netbeans IDE.

main.c contains a program which prints out the information of the connected NRF24L01 device and ping demo.
you may need to upload the Arduino sketch in 'pingpair_dyn_arduino_pongback' directory to a Arduino board in order for both Beaglebone and Arduino to run interactively.

