## Digital Volume Control
In the image of the CSO [here](https://github.com/kiteretro/Circuit-Sword/wiki/Circuit-Sword-Original-V1.1E#bottom) there is a rocker navigation switch that is unpopulated. This can act as a digital volume control, meaning the switch will trigger a volume UP or DOWN.

1. Get and solder the nagivation swith (e.g. https://www.aliexpress.com/item/10pcs-lever-and-Push-switch-momentary-operation-by-lever-and-center-push-using-a-single-knob/32795557524.html)
2. Edit the arduino code at this line: https://github.com/kiteretro/Circuit-Sword/blob/master/kite-arduino/CS_FIRMWARE/config.h#L64 and change to:
``` c
#define USE_VOLUME_DIGITAL
```
3. Upload to Arduinio

This converts the CC1 and CC2 (the 5th and 6th front buttons) to VOLUP and VOLDOWN (used by the new volume switch) .. meaning you can't use the volume rocker AND the 5th and 6th front buttons in your build.