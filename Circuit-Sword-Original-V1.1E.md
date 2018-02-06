# Hardware Overview
The following images should generally what the product is and what it includes:
![Overview](https://i.imgur.com/f2y7ulx.jpg)
![Back Board](https://i.imgur.com/tFAHmIA.jpg)
![Back board 2](https://i.imgur.com/jsqHT8o.jpg)
![Power Switch](https://i.imgur.com/3NICQzA.jpg)
![Fan](https://i.imgur.com/oiyyRez.jpg)

# Board Overview
## LEDs
### ALL LEDs
The following image shows the states of all the main LEDs on the board:
[[images/CSO_V1.1E_ALL_LEDs.png]]

### LED Extensions
The following image shows the wiring of the main status LEDs if you wish to re-route them elsewhere. NOT that the charging LED is NOT common GND and MUST use the two wires as detailed:
[[images/CSO_V1.1E_LEDs.png]]

## TOP
The following image shows the front/top of the board and points out useful things:
[[images/CSO_V1.1E_FRONT.png]]

# BOTTOM
The following image shows the back/bottom of the board and points out useful things:
[[images/CSO_V1.1E_BACK.png]]

# PCB Modifications
## Digital Volume Control
In the image above there is a rocker navigation switch that is unpopulated. This can act as a digital volume control, meaning the switch will trigger a volume UP or DOWN.

1. Get and solder the nagivation swith (e.g. https://www.aliexpress.com/item/10pcs-lever-and-Push-switch-momentary-operation-by-lever-and-center-push-using-a-single-knob/32795557524.html)
2. Edit the arduino code at this line: https://github.com/geebles/Circuit-Sword/blob/master/kite-arduino/CS_FIRMWARE/config.h#L64 and change to:
```
#define USE_VOLUME_DIGITAL
```
3. Upload to Arduinio

This converts the CC1 and CC2 (the 5th and 6th front buttons) to VOLUP and VOLDOWN (used by the new volume switch) .. meaning you can't use the volume rocker AND the 5th and 6th front buttons in your build.