# Updating the Firmware
The Circuit Sword has an ATMEGA32u4 (Arduino Leonardo) chip that controls the buttons, brightness, and a few other functions. Sometimes you might need to update the software running on this chip to add new features.

**AS A GENERAL RULE - Updating the Arduino is not required unless something specifically mentions doing it. The code when shipped is fully updated and supported and works for all functionality.**

The Arduino is updatable by USB, and the easiest way is to do it from a computer rather than from the Pi.

## Prepare Circuit Sword for Computer-USB Connection
To connect to the PC, you need to:

1. Turn off and unplug USB from Circuit Sword
2. Set the [config switches](https://github.com/geebles/Circuit-Sword/wiki/Configuration-Switches) to "HUB-PASSTHRU" and "PROG-EN"
3. Plug in USB cable to PC and Circuit Sword
4. Turn the Circuit Sword on using the power switch

At this point, your computer will recognise the following new devices:

[[images/CSO/CS_USB_DEVICES.png]]

## Install Arduino Software
1. Download the [Arduino software](https://www.arduino.cc/en/Main/Software)
2. Install

## Preparing the software
3. Download the latest source code (e.g. cloning this repo)
4. Browse to `Circuit-Sword/kite-arduino/CS_FIRMWARE/`
5. Double click `CS_FIRMWARE.ino`
6. In the editor click `Sketch -> Include Libraries -> Manage Libraries`
7. Search for `HID-Project` and install it
8. Click on the `config.h` tab
9. Uncomment the HARDWARE define near the top to select your board
10. Uncomment any feature that you want to enable
11. Click `Tools -> Board -> Arduino Leonardo`
12. Click `tools -> Port -> COMX` (where X if your COM port labelled Leonardo)
13. Click upload, and check the bottom of screen for errors or `Upload Done`
