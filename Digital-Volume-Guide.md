# Digital Volume Control

## Volume Options

1. Use the MODE + UP/DOWN button combo to adjust the volume
2. Solder a volume rocker (navigation switch) to the board
3. Solder 2x individual buttons to the navigation switch pads

## Digital Volume Buttons (rocker or buttons)
In the image of the CSO [here](https://github.com/kiteretro/Circuit-Sword/wiki/Circuit-Sword-Original-V1.1E#bottom) there is a rocker navigation switch that is unpopulated. This can act as a digital volume control, meaning the switch will trigger a volume UP or DOWN. 

1. Get and solder the nagivation swith (e.g. https://www.aliexpress.com/item/10pcs-lever-and-Push-switch-momentary-operation-by-lever-and-center-push-using-a-single-knob/32795557524.html) OR solder your own 2x buttons to the pads.
2. Edit the arduino config.h file: https://github.com/kiteretro/Circuit-Sword/blob/master/kite-arduino/CS_FIRMWARE/config.h and change the config near the top from:
``` c
//#define USE_VOLUME_DIGITAL
```
To:
``` c
#define USE_VOLUME_DIGITAL
```
3. Upload to Arduinio

This converts the CC1 and CC2 (the 5th and 6th front buttons) to VOLUP and VOLDOWN (used by the new volume switch) .. meaning you can't use the volume rocker AND the 5th and 6th front buttons in your build.

## Alternative Pins for Digital Volume Control
If you don't want to lose the CC1 and CC2 (5th and 6th front buttons) there is an alternative. In the Arduino code, change the config near the top of config.h from:
``` c
//#define USE_VOLUME_DIGITAL
//#define USE_ALT_PINS_VOLUME_DIGITAL
```
To:
``` c
#define USE_VOLUME_DIGITAL
#define USE_ALT_PINS_VOLUME_DIGITAL
```

This will enable the use of "RX0" and "TX0" as VOL DOWN and VOL UP.

In order to change the hardware, you will need to use a knife and cut the traces here:

[[images/CSO/CSO_DIGITAL_AUDIO_1.PNG]]

And then solder 2x wires here:

[[images/CSO/CSO_DIGITAL_AUDIO_2.PNG]]