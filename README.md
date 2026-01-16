# Gamebooy-Multi-sensor-Cartdrige
A gameboy cartridge that can be used as a home multi-sensor or taken with you on adventures

# Parts Needed & Construction




# Auduino Flashing

The heart of this flash cart is an Atmega32U-MU microcontroller. The board has been designed with a USB-C port to make flashing the microcontroller easy. First, you will need to download and install the [Arduino IDE](https://docs.arduino.cc/software/ide/).

# Links to Digikey/Mouser Cart Orders
[Digikey order](https://www.digikey.com/short/mhdbv30d)
# Sensors
The board utilizes two sensors (BME680 & HMC5883L) that can monitor altitude, barometric pressure, humidity, temperature, and a compass. It also comes with a real-time clock (BQ32000DR). 

# Test Points & Jumpers

There are nine test points placed on this cartridge:

- 5V - checks the 5V line from Pin 1 (VCC)
- 3.3 V - checks the 3.3V line leaving pin 6 (VOUT) of the 3.3V regulator (MIC5255-3.3)
- BAT - checks the CR12XX battery voltage
- CMD - checks to see if the command pulse is triggered to the NAND/NOR logic for writing and reading data from the ATmega328
- SDA - cheks the SDA I<sup>2</sup>C data line. Both the sensor (BME680) & clock (DS13072N+) are connected to the same test point
- SCL -cheks the SCL I<sup>2</sup>C data line. Both the sensor (BME680) & clock (DS13072N+) are connected to the same test point
- RESET - pad for soldering to a XXX
- MISO - XXXX
- MOSI - XXXX
- SCLK - XXXX

There is one jumper pad that must be soldered prior to powering on the board.

- JP2 - jumper 2 is an output driver for the 7-bit address for the sensor (BME680), and connects pin 6 (SDO) to either 3.3V or GND. The jumper must be bridged prior to powering the device for the first time. The 7-buit address is 111011x. Connecting JP2 to 3.3V results in a slave address of 1110111 (0x77) and connecting JP2 to GND results in a slave address of 1110110 (0x76).

# Board Fitment 

The shape of this board was originally meant to mimic original Game Boy circuit boards as closely as possible. Unfortunately, when placed in some aftermarket Game Boy cartridge shells (like those from Cloud Game Store), the circuit board has a lot of freedom to rotate around the main screw hole in the bottom-middle of the cartridge. This can cause misalignment when you put it in a Game Boy, which can cause a game to either not load properly (garbled Game Boy logo) or shut off the Game Boy because of a short circuit. This isn't dangerous or anything, just annoying.

In order to make the boards fit nicer in any kind of shell, I added extended tabs of circuit board material to the edges of the cartridges to keep it from rotating too much in shells, which was suggested to me by [orangeglo](https://github.com/orangeglo)! (Thanks!)

If you're having trouble fitting the circuit board into a shell, because the tabs interfere with the cart edges, you can safely sand or trim them down as there is no copper within the tabs themselves. The only shell that appears to require any kind of trimming are Kitsch-Bent shells.

_Copied from MouseBite Labs' README_

# Links & Acknowledgements

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/O5O21S4YC9)

[GBxCart](https://www.gbxcart.com/)

[Lesserkuma's Flash GBX Software](https://github.com/lesserkuma/FlashGBX)

This board is modified from [MouseBite Labs](https://github.com/MouseBiteLabs/Game-Boy-Cartridges)' cartridges

https://tinkerer.us/projects/homebrew-gameboy-cartridge.html

Thanks to [Orangeglo](https://github.com/orangeglo) for his help in designing this cartridge

# Revision History

**V 1.1**

-Updated board schematics, corrected impropper voltage routing, and added a magnetometer sensor.

**V 1.0**

-Initial Creation

# License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. You are able to copy and redistribute the material in any medium or format, as well as remix, transform, or build upon the material for any purpose (even commercial) - but you **must** give appropriate credit, provide a link to the license, and indicate if any changes were made.
