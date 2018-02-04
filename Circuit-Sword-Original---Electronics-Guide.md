# Overview
This small guide will walk you through the basic steps of how the electronics work for the Circuit Sword Original. The actual plastic hardware case used is pretty much open ended and entirely up to you, but there are guides on the right hand menu that will help in those areas. This section is specifically about the board and electronics.

# Tools Needed
The follow would be REALLY useful to have, and I would not recommend to continue without them:
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

All the LEDs should come on at this point. As soon as you release the button it should all power off. The most important LEDs are the 5x power LEDs right below the compute module connector. Those show that all voltage rails are working. If any LED is out, contact the forum/email for support.

4. Unplug USB cable, and plug in battery
5. Plug in USB cable
6. The PG and CHRG LEDs should be lit (CHRG may only light briefly if the battery is full)

## 2. First boot
Now that basic power looks good