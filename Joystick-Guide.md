# How to install a joystick
## Fitting the joystick
The Circuit Sword has 2x joystick ports, both are labelled with the pinout where X is left/right and Y is up/down. See the board itself for the pinout and match up yourself to the included 4pin JST SH connectors.

[[images/CSO/CSO_JOYSTICK_CONN1.png]]

## Calibrating the joystick
When the joystick is connected, it will not function until it is calibrated. The calibration sequence detects if a joystick is connected and sets the min and max based on the actual joystick you have. If a joystick is not connected, the calibration won't enable it.

1. Power off everything
2. (Optional) Remove the SD (as we do not want the Circuit Sword to boot)
3. Hold the START button
4. Turn the power switch ON
5. After 3 seconds, release the START button and slowly rotate the joystick through its entire motion. You will have 10 seconds to do this
6. (Optional) Connect up to a PC to see the joystick output (tips [here](https://github.com/geebles/Circuit-Sword/wiki/Configuration-Switches))
7. Turn off, put SD in, boot, configure gamepad

## If any axis are inverted/wrong way round
You will need to edit the Arduino code, see here: https://github.com/geebles/Circuit-Sword/blob/master/kite-arduino/CS_FIRMWARE/config.h#L138-L141

You will need to comment/uncomment the axis in question. For example if left/right is OK but up/down is inverted, you need to change the Y1 axis from:
``` c
#define INVERT_Y1        // Invert the Y1 axis
```

To:
``` c
//#define INVERT_Y1        // Invert the Y1 axis
```

Be sure to save and [upload](https://github.com/geebles/Circuit-Sword/wiki/Updating-Arduino-(button-controller)-Firmware)
