# USB-PD fan driver

This is a completely untested, mostly routed PCB that uses a cheap MCU to trigger a 12V USB-PD sink, to drive a computer box fan.
There are two touch pads connected 
Designed to be as cheap as possible, using the [CH32X035 MCU](https://www.wch-ic.com/products/CH32X035.html).
Most firmware development could be done using the inbuilt USB bootloader or the [UCPD adapter](https://github.com/wagiminator/CH32X035-USB-PD-Adapter) sample code from Stefan Wagner. More simple example firmwares for CH32X035 live here: [CH32V003fun examples](https://github.com/cnlohr/ch32v003fun/tree/master/examples_x035)
There are LEDs to indicate the fan speed and two touch buttons to make it go faster and slower.
Not sure if I will finish this, but someone else could!

Evan Kahn 2025
