# Known Issues and Workarounds
This page will detail any known issues and potential ways to avoid or solve them.

## Issue 1 - The MODE button is very short and doesn't poke out much.
**Cause:** This happened due to mis-communication when the product was manufactured

**Solution 1:** Buy replacement longer buttons ([example](https://www.aliexpress.com/item/100Pcs-Tactile-Switch-Momentary-Tact-6x6x6-6-6-6mm-Middle-pin-2pins/32727102870.html))

**Solution 2:** Make some kind of extension (3D print a hat for it?)

## Issue 2 - The volume with button combo is very slow to update
**Cause:** The very first software image had a second delay between each check (at best case!). This ONLY affect the release v1.0.0 so if you used a release later than this, you don't need to update.

**Solution 1:** Update the software with [these simple steps](https://github.com/kiteretro/Circuit-Sword/wiki/Updating-the-Software-(running-on-Pi)).

## Issue 3 - When in the 'raspi-setup' menu, the buttons are mapped wrong
**Cause:** ES/Retropie mapped them wrong

**Workaround 1:** Follow [these steps](https://github.com/kiteretro/Circuit-Sword/wiki/Updating-the-Software-(running-on-Pi)#enable-ssh) in order to use the menu. In summary: press UP/DOWN to pick an item, then press RIGHT to change the selector to "OK" and then press "B" to select it! (Usually A is select, but in this menu only it is now "B"). Same applies to when enabling settings (e.g. SSH); press left/right to select option and "B" to select it.

## Issue 4 - WiFi doesn't work
**Cause:** Most likely the back board is contacting the wifi chip and shorting something

**Solution 1:** Place kapton tape over the WiFi chip, use a couple of layers

## Issue 5 - Digital volume control doesn't work at all
**Cause:** Most likely after a joystick calibration that has enabled the use of the analog volume dial (but none is present)

**Solution 1:** The software and Arduino need updating. The easiest way is to do the following:
1. Enable WiFi
2. SSH in
3. `cd Circuit-Sword`
4. `sudo ./update.sh YES`
5. `sudo apt-get install avrdude`
6. `sudo ./flash-arduino.sh`
7. `sudo reboot`
8. Power off normally. Then HOLD START AND POWER ON (to do a joystick calibration)
9. Done! Adjust volume as normal.

## Issue 6 - Cannot connect CSO to PC (unknown device)
**Cause:** For reasons unknown, plugging in to a USB3 enabled port doesn't always work.

**Solution 1:** One method is to plug a USB 2.0 HUB into your PC, and then plug the CSO into the HUB

## Issue 7 - Cannot update "retropie-scripts" or certain packages/updates won't install
**Cause:** Early versions of the image edited an unused file, and this prevents it from updating itself

**Solution 1:** Follow these steps:
1. Enable WiFi and SSH in
2. `cd RetroPie-Setup`
3. `git fetch --all`
4. `git reset --hard origin/master`
5. `sudo reboot`

## Issue 8 - Joystick 2 does not work!
**Cause:** Thanks to a typo, it wasn't enabled properly..

**Solution 1:** Update the Arduino code using any of the methods [here](https://github.com/kiteretro/Circuit-Sword/wiki/Updating-Arduino-(button-controller)-Firmware)