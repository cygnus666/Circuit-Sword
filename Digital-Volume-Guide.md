# Digital Volume Control

## Volume Options

1. Use the MODE + UP/DOWN button combo to adjust the volume
2. Solder a volume rocker (navigation switch) to the board
3. Solder 2x individual buttons to the navigation switch pads

## Digital Volume Buttons (rocker or buttons)
In the image of the CSO [here](https://github.com/kiteretro/Circuit-Sword/wiki/Circuit-Sword-Original-V1.1E#bottom) there is a rocker navigation switch that is unpopulated. This can act as a digital volume control, meaning the switch will trigger a volume UP or DOWN. 

1. Get and solder the nagivation swith (e.g. https://www.aliexpress.com/item/10pcs-lever-and-Push-switch-momentary-operation-by-lever-and-center-push-using-a-single-knob/32795557524.html) OR solder your own 2x buttons to the pads.
2. [Update](https://github.com/kiteretro/Circuit-Sword/wiki/Updating-the-Software-(running-on-Pi)) and [flash](https://github.com/kiteretro/Circuit-Sword/wiki/Updating-Arduino-(button-controller)-Firmware#via-the-raspberry-pi) the latest arduino code. It will be enabled by default without any configuration needed. It uses the `RX` and `TX` pins by default.

### Hardware version 1.1E requires a hardware mod. All other versions do not!

<details>
<summary>Click to expand</summary>
In order to change the hardware, you will need to use a knife and cut the traces here:

[[images/CSO/CSO_DIGITAL_AUDIO_1.PNG]]

And then solder 2x wires here:

[[images/CSO/CSO_DIGITAL_AUDIO_2.PNG]]
</details>
