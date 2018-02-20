# Known Issues and Workarounds
This page will detail any known issues and potential ways to avoid or solve them.

## Issue 1 - The MODE button is very short and doesn't poke out much.
**Cause:** This happened due to mis-communication when product was manufactured

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

**Workaround 1:** Place kapton tape over the WiFi chip, use a couple of layers

## Issue 5 - Digital volume control doesn't work at all
**Cause:** Most likely after a joystick calibration that has enabled the use of the analog volume dial (but none is present)

**Solution 1:** Follow the steps to update the software AND the Arduino here: https://github.com/kiteretro/Circuit-Sword/issues/17#issuecomment-366892950