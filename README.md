# USB-PD fan driver

![Screenshot 2025-01-10 140730](https://github.com/user-attachments/assets/59eb2abe-d36e-494e-83cc-90c2db527197)

This is a completely untested, mostly routed PCB that uses a cheap MCU to trigger a 12V USB-PD sink, to drive a computer box fan. Entire BOM cost should only be $2-$3, no uncommon components. Might have to hand-solder the fan header. You could also use an angled fan header if you wanted.

I started designing this because I was annoyed about not having a desktop fume extractor that I could easily run off a laptop charger. I got busy / lazy and don't actually want to finish it, but if someone wants to adopt it that would be awesome! I have a handful of the CH32X035 preordered on JLCPCB, so the riskiest $10 of the project budget is already a sunk cost.

I designed this with 12V PWM fans in mind, but it occurs to me that if you want an amount of static pressure appropriate for fume extraction the move might be to use a 20V PDO. The SY8201 step-down should be able to support that no problem. Just make sure you don't plug it into a 12V fan then.

It is a Kicad 7 project. You could open and save it in Kicad 8 and force push it if you wanted, I don't care.

Designed to be as cheap as possible, using the [CH32X035 MCU](https://www.wch-ic.com/products/CH32X035.html).

99% of this design is derived from Stefan Wagner's repos:
https://github.com/wagiminator/Development-Boards
https://github.com/wagiminator/CH32X035-USB-PD-Adapter

Most firmware development could be done using the inbuilt USB bootloader or the [UCPD adapter](https://github.com/wagiminator/CH32X035-USB-PD-Adapter) sample code from Stefan Wagner. More simple example firmwares for CH32X035 live here: [CH32V003fun examples](https://github.com/cnlohr/ch32v003fun/tree/master/examples_x035)

There are LEDs to indicate the fan speed and two touch buttons to make it go faster and slower. Since there's a tach pin, you could do some pretty delightful UI stuff by making the line of LEDs strobe at the exact speed that the rotors are turning, which would make this into a fun desk toy.

I don't do a lot of work with motors and maybe would like someone to take a second look at the fan drive circuit. I followed [this](https://noctua.at/pub/media/wysiwyg/Noctua_PWM_specifications_white_paper.pdf) white paper. Do I need a flyback diode or something? More decoupling capacitors?

I remember spending a comically long time trying to find an in-stock LCSC alt for the 4-pin 2.54mm fan connector (Molex 470533000), it looks like it might be in "Molex actually defends that patent" territory. Oh well. Buy them on Amazon and solder them yourself, or knock yourself out on Aliexpress.
On the plus side, this means there are no through-hole parts, which will knock a day and a couple dollars off the final JLCPCB bill.

Evan Kahn 2025
