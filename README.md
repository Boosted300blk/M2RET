M2RET
=======

Reverse Engineering Tool running on Macchina M2 Hardware

A fork of the GVRET project.

#### Requirements:

You will need the following to be able to compile the run this project:

- [Arduino IDE](https://www.arduino.cc/en/Main/Software) 1.5.4 or higher (tested all of the way up to 1.6.12)
- [due_can](https://github.com/collin80/due_can) - Object oriented canbus library for Arduino Due compatible boards.
- [due_wire](https://github.com/collin80/due_wire) - An alternative I2C library for Due with DMA support.
- [Arduino_Due_SD_HSCMI](https://github.com/collin80/Arduino_Due_SD_HSCMI) - SD card support library
- [SD_HSCMI](https://github.com/collin80/SD_HSCMI) - Another SD support library
- [LIN](https://github.com/collin80/LIN) - Support for the dual LIN ports on the M2
- [SamNonDuePin](https://github.com/collin80/SamNonDuePin) - Allows access to pins not mapped on standard Arduino Due boards
- [SW_CAN](https://github.com/collin80/SW_CAN) - Single wire CAN support for M2 board

Note, the last five libraries are all copied from https://github.com/macchina/m2-libraries but have been modified. You will need the versions found above in order to compile the M2RET firmware yourself.

All libraries belong in %USERPROFILE%\Documents\Arduino\libraries (Windows) or ~/Arduino/libraries (Linux/Mac).
You will need to remove -master or any other postfixes. Your library folders should be named as above.

The canbus is supposed to be terminated on both ends of the bus. This should not be a problem as this firmware will be used to reverse engineer existing buses.

#### The firmware is a work in progress. What works:
- CAN0 and CAN1 are operational
- EEPROM can be used to save settings between start ups
- Text console is active (configuration and CAN capture display)
- Can connect as a GVRET device with SavvyCAN
- Able to automatically start up and log all traffic to sdCard. Not stable at high bus loads just yet.
- LAWICEL support (very basic)
- Blinken Lights!

#### What does not work:
- Either LIN bus
- Single wire CAN
- Anything you attach to the XBEE port
- Any of the digital I/O pins on the 26 pin connector

#### License:

This software is MIT licensed:

Copyright (c) 2014-2017 Collin Kidder, Michael Neuweiler, Charles Galpin

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

