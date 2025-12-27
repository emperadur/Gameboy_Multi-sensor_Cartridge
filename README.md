# Gamebooy-Multi-sensor-Cartdrige
A gameboy cartridge that can be used as a home multi-sensor or taken with you on adventures

# Test Points & Jumpers

There are four test points placed on this cartridge

- 5V - checks the 5V line from Pin 1 (VCC)
- 3.3 V - checks the 3.3V line leaving pin 6 (VOUT) of the 3.3V regulator (XC6206P332DR-G)
- BAT - checks the CR12XX battery voltage
- SDA - cheks the SDA I<sup>2</sup>C data line. Both the sensor (BME680) & clock (DS13072N+) are connected to the same test point
- SCL -cheks the SCL I<sup>2</sup>C data line. Both the sensor (BME680) & clock (DS13072N+) are connected to the same test point

There are two jumper pads

- JP1 - xxx
- JP2 - jumper 2 is an output driver for the 7-bit address for the sensor (BME680), and connects pin 6 (SDO) to either 3.3V or GND. The jumper must be bridged prior to powering the device for the first time. The 7-buit address is 111011x. Connecting JP2 to 3.3V results in a slave address of 1110111 (0x77) and connecting JP2 to GND results in a slave address of 1110110 (0x76).

# Cartridge 

The shape of this board was originally meant to mimic original Game Boy circuit boards as closely as possible. Unfortunately, when placed in some aftermarket Game Boy cartridge shells (like those from Cloud Game Store), the circuit board has a lot of freedom to rotate around the main screw hole in the bottom-middle of the cartridge. This can cause misalignment when you put it in a Game Boy, which can cause a game to either not load properly (garbled Game Boy logo) or shut off the Game Boy because of a short circuit. This isn't dangerous or anything, just annoying.

In order to make the boards fit nicer in any kind of shell, I added extended tabs of circuit board material to the edges of the cartridges to keep it from rotating too much in shells, which was suggested to me by orangeglo! (Thanks!)

If you're having trouble fitting the circuit board into a shell, because the tabs interfere with the cart edges, you can safely sand or trim them down as there is no copper within the tabs themselves. The only shell that appears to require any kind of trimming are Kitsch-Bent shells.

_Copied from MouseBite Labs' README_

# Links & Acknowledgements

https://www.gbxcart.com/

https://github.com/lesserkuma/FlashGBX

This board is modified from MouseBite Labs' cartridges

https://github.com/MouseBiteLabs/Game-Boy-Cartridges

https://tinkerer.us/projects/homebrew-gameboy-cartridge.html

Thanks to Orangeglo https://github.com/orangeglo for his help in designing this cartridge

# Revision History

**V 1.0**

-Initial Creation
