# PicoSerial
When I was designing the FRC ESP32 DevKit Lite, I discovered a problem!
The USB-Serial chip was too expensive (~$6 a piece)!
This project aims to solve this problem in a cheap and effective way using a RP2350 (~$1.40 each) and its USB controller and serial functionality to replicate expensive converter chips but at a fraction of the price.

The Raspberry Pi Debug Probe is a good product, but I found that it has a few improvements to be made.
In addition to that, this project may be embedded in other future projects to replace the USB-Serial chip.

1. The Debug Probe has a USB Micro-B connection, which is very fragile and inferior to USB-C
2. It costs too much (~$17 each, which makes it prohibitively expensive to embed)
3. For my purposes, I only need serial programming, not swd. (but swd/other debug protocols most likely can be added to this project using an addon board)
4. This version is a USB-serial converter board, similar to this one
5. The Debug Probe does not have a "FTDI" style 6 pin connector which is used on many devices, but instead has a 3 pin JST connector.
   - This works but does not have auto reset, so if the probe was used to program a microcontroller, buttons may need to be pressed in order to put it into the bootloader
   - For devices that use a 3 pin JST connector, another addon board or adapter cable could be made.
   - This version aims to have auto reset implemented to make end-users' lives more convenient

However, this device will probably run the open-source Picoprobe software (or modified version), made by Raspberry Pi, that the official Raspberry Pi Debug Probe uses.

Disclaimer:

Not affiliated with FTDI or Raspberry Pi. All trademarks properties of their respective owners.
