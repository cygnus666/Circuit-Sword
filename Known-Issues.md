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

If it still doesn't work and volume is still stuck on 100% or bounces all over the place, remove the line `#define USE_ANALOG_VOLUME` in the [config.h](https://github.com/kiteretro/Circuit-Sword/blob/master/kite-arduino/CS_FIRMWARE/config.h#L69) file (you need to follow the steps about download Arduino IDE to write the custom firmware).

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

## Issue 9 - Some LCD colours are a bit weird
**Cause:** Solder balls appear to get stuck at the back of the LCD connector, at the top of the plastic. During manufacture these can melt causing two pins to join together that shouldn't. These are typically hard to see with eyes alone, a high detail photo is needed on the BACK of the LCD connector on the board, at an approx 45 degree angle with plenty of light. Customer found issue [here](https://sudomod.com/forum/viewtopic.php?f=51&t=6122#p62848)

<details>
<summary>Image of solder bridge - Click to expand</summary>
[[https://i.imgur.com/AZWvyKo.jpg]]
</details>
&nbsp;

**Solution 1:** Using a very sharp knife, carefully cut through the bridge. Alternatively send me an email and we'll sort out a repair.

**Solution 2:** Using plenty of flux and a dry iron, you can remove the bridges. See Lee's excellent video here: https://www.youtube.com/watch?v=HbeHoqdrTOg

## Issue 10 - PiFBA sound runs too fast
**Cause:** Unknown, likely tied to some kind of screen timings. Found by makemao [here](https://github.com/kiteretro/Super-AIO/issues/6#issuecomment-416043518).

**Solution:** Follow these steps (only applies to 320x240 LCD):
Edit the config.txt (SD in PC, or /boot/config.txt) and change the timing value:

hdmi_timings=320 1 20 30 38 240 1 4 3 10 0 0 0 60 0 **6400000** 1

## Issue 11 - cs-hud fails to run on Retropie 4.3 due to missing libpng16
**Cause:** The 4.3 release uses the older kernel, 4.4 uses the raspbian 'stretch' image and includes this library.

**Solution:** An issue has already been raised and the user has solved it, information can be found here: https://github.com/kiteretro/Circuit-Sword/issues/65

## Issue 12 - No boot / black screen only
**Symptoms:** All power LEDs are good, the SD has been written successfully with an image from the 'releases' tab (when inserted into a PC it shows as a 56MB drive, regardless of real SD size (this is expected)), however when powered on there is nothing but black shown on the LCD. The 'PGOOD' and 'USBHUB' LEDs are not lit either (showing that the CM3 hasn't actually booted at all). Existing issue [here](https://github.com/kiteretro/Circuit-Sword/issues/69).

**Cause:** The SD connector on the board has moved slightly when manufacturing and in some rare cases when reflowed the pins don't make full contact and so it appears to the Pi that the SD card isn't connected.

It is possible to check if this is the case by probing the following pins with a multimeter in resistance mode (where it will beep when a contact is made, the expectation of a working board is that each pair of pins will beep when probed from each end):

<details>
<summary>Image of SD pinouts - Click to expand</summary>
[[https://i.imgur.com/ijs9VrV.jpg]]
</details>
&nbsp;

**Solution:** Send kite an email (kite@kitesitemshop.com) describing this problem and I will replace your board. You will need to return the faulty board to the address provided in the email reply. The repair is to re-flow the solder (either by hot air or a fine tipped iron) for the pins on the INSIDE of the SD slot (that can be seen through the little cutout near the edge of the board. Note that it's the soldered pins, not the gold ones that make contact with the actual SD card.