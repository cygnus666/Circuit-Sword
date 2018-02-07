# Overview
This small guide will walk you through the basic steps of how the electronics work for the Circuit Sword Original. The actual plastic hardware case used is pretty much open ended and entirely up to you, but there are guides on the right hand menu that will help in those areas. This section is specifically about the board and electronics.

# Tools Needed
The following would be REALLY useful to have, and I would not recommend to continue without them:
* Kapton tape (electrical tape is NOT good enough)
* Double sided sticky tape
* Double sided foam tape
* Screwdrivers/tools
* Digital Multimeter (seriously, they're cheap, I recommend on a budget the ANENG AN8008)
* Soldering iron
* USB C Cable
* Dremel/rotary tool
* Files, drills, etc
* Sharp knife

# Electronics Guide
## 1. Basic sanity check
The first thing we should do is check that the board is safe and powers up without issue. We can do this using ONLY the Circuit Sword main PCB and a USB C cable. DO NOT put the Compute Module in yet, or battery, or connect anything else up to it.

1. Plug in the USB C cable to the board and into a Computer/USB/etc
2. The 'PG' RED LED should be lit (to the right of the battery connector)
3. Press and hold the 'power button' which is located to the RIGHT of the battery connector

All the LEDs should come on at this point (see [here](https://github.com/geebles/Circuit-Sword/wiki/Circuit-Sword-Original-V1.1E#all-leds) for more information). As soon as you release the button it should all power off. The most important LEDs are the 5x power LEDs right below the compute module connector. Those show that all voltage rails are working. If any LED is out, contact the forum/email for support.

4. Unplug USB cable, and plug in battery
5. Plug in USB cable
6. The PG and CHRG LEDs should be lit (CHRG may only light briefly if the battery is full)

## 2. First boot
Now that basic power looks good, you can proceed to insert the Compute Module into the holder, insert a flashed SD, and connect up the back board:

7. Insert Compute Module into holder, and connect up the FPC and back board as shown below.
8. Insert a pre-imaged SD card into the SD slot (click [here](https://github.com/geebles/Circuit-Sword/wiki/Flashing-Software-onto-the-Compute-Module) for how-to)
9. Insert the LCD into the LCD connector (NOTE: Be very careful with the LCD connector, you do not want to pull hard on it otherwise it will break the delicate plastic tabs)

_Note that the [heatsink and fan](https://github.com/geebles/Circuit-Sword/wiki/Fan-and-Heatsink) aren't required for the first boot testing. Nothing bad will happen without them. Connect like so:_

[[images/CSO/CSO_V1.1E_BASIC_CONNECTIONS.jpg]]

_The back board connector goes BLUE SIDE UP on both ends_
[[images/CSO/CSO_V1.1E_BBCONN1.jpg]]
[[images/CSO/CSO_V1.1E_BBCONN2.jpg]]

_The LCD connector is PINS SIDE UP_
[[images/CSO/CSO_V1.1E_LCDCONN1.jpg]]

10. Slide the switch ON
11. The Compute Module should boot, it will first resize the partition and reboot. It will take 2-3mins on first boot to configure everything. Subsequent boots WILL be quicker so just be patient for now :)
12. Once booted, use a rubber membrane to configure the input as instructed on screen
13. Done! See the retropie website for further steps https://retropie.org.uk/docs/Controller-Configuration/

## 3. Next steps
Now that the electronics are tested to be working, the only extra things you might want to do are the back buttons and joystick (optional) as these require soldering to complete. Most likely you'll want to assemble it into your case!
