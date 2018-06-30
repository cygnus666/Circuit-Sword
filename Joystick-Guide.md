# How to install a joystick
## Fitting the joystick
The Circuit Sword has 2x joystick ports, both are labelled with the pinout where X is left/right and Y is up/down. See the board itself for the pinout and match up yourself to the included 4pin JST SH connectors.

[[images/CSO/CSO_JOYSTICK_CONN1.png]]

## Calibrating the joystick (NEW METHOD)
Follow the steps here to use the interactive menu: https://github.com/kiteretro/Circuit-Sword/wiki/Configuring-the-software-without-flashing-the-arduino

## If any axis are inverted/wrong way round
Follow the steps here to use the interactive menu: https://github.com/kiteretro/Circuit-Sword/wiki/Configuring-the-software-without-flashing-the-arduino

## Calibrating the joystick (OLD METHOD)
When the joystick is connected, it will not function until it is calibrated. The calibration sequence detects if a joystick is connected and sets the min and max based on the actual joystick you have. If a joystick is not connected, the calibration won't enable it.

1. Power off everything
2. (Optional) Remove the SD (as we do not want the Circuit Sword to boot)
3. Hold the START button
4. Turn the power switch ON
5. After 3 seconds, release the START button and slowly rotate the joystick through its entire motion. You will have 10 seconds to do this
6. (Optional) Connect up to a PC to see the joystick output (tips [here](https://github.com/kiteretro/Circuit-Sword/wiki/Configuration-Switches))
7. Turn off, put SD in, boot, configure gamepad

# PSP Joystick
[[images/CSO/PSP.jpg]]

# Switch Joystick
[[images/CSO/JOYCON.jpg]]