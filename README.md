# USB-PD fan driver

This is a completely untested, mostly routed PCB that uses a cheap MCU to trigger a 12V USB-PD sink, to drive a computer box fan. Entire BOM cost should only be $2-$3, no uncommon components. Might have to hand-solder the fan header.

I got busy / lazy and don't actually want to finish this, but if someone wants to adopt it that would be awesome!

It is a Kicad 7 project. You could open and save it in Kicad 8 and force push it if you wanted, I don't care.

Designed to be as cheap as possible, using the [CH32X035 MCU](https://www.wch-ic.com/products/CH32X035.html).

Most firmware development could be done using the inbuilt USB bootloader or the [UCPD adapter](https://github.com/wagiminator/CH32X035-USB-PD-Adapter) sample code from Stefan Wagner. More simple example firmwares for CH32X035 live here: [CH32V003fun examples](https://github.com/cnlohr/ch32v003fun/tree/master/examples_x035)

There are LEDs to indicate the fan speed and two touch buttons to make it go faster and slower. Since there's a tachometer, you could do some pretty delightful UI stuff by making the line of LEDs strobe at the exact speed that the rotors are turning, which would make this into a fun desk toy.

I don't do a lot of work with motors and maybe would like someone to take a second look at the fan drive circuit. I followed [this](https://noctua.at/pub/media/wysiwyg/Noctua_PWM_specifications_white_paper.pdf) white paper. Do I need a flyback diode or something? More decoupling capacitors?

Also, it's pretty hard to find the through-hole fan connector on LCSC, so the part link is to Aliexpress. Con: there's one manual assembly step. Pro: we have sprung literally none of the typical JLCPCB added-cost traps. 

Evan Kahn 2025
