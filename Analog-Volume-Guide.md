# Analog Volume

## Volume Options
You have the following options in regards to adjusting the system volume:

1. Use the MODE + UP/DOWN button combo to adjust the volume
2. Use the optional analog volume back board (which replaces the HDMI back board) and puts the volume pot in place of the HDMI connector
3. Place your own volume wheel in conjunction with option #1 and connect to the "ANALOG VOL" connector (JST SH 1.0mm 3pin)

## Volume Wheel (any)
The Circuit Sword does not use a voltage divider or potentiometer to adjust the volume, instead it uses the linux/pi volume control that is built in. This is the same as pressing START on the menu and adjusting the volume slider.

In order to adjust the volume using combo keys and any other input from buttons, which are all handled by the Arduino, the Arduino itself needs to remember the volume level. The OSD Script that runs in the background periodically reads the volume from the Arduino and if it is different to what is already set last, it send the command to adjust the volume.

By default the Arduino waits for combo key input, and adjusts it's internal value.. however there is an analog pin designated for analog volume control, which if connected to a 10k pot as a 3.3v voltage divider, will give you a range of volume from 0-100%.

In order to ENABLE to analog volume pot, you must do:

### New method to enable
1. Follow instructions here: https://github.com/kiteretro/Circuit-Sword/wiki/Configuring-the-software-without-flashing-the-arduino and select the menu option to "toggle analog volume" so that it shows "1" on the status.

### Old method to enable
<details>
  <summary>Click to expand</summary>

1. Connect up the pot to the ANALOG VOL connector as a voltage divider (signal in middle, GND at bottom and 3.3V at top) 
2. Turn everything off and remove SD card to prevent Pi booting
3. Turn volume to the MIDDLE (or the top, basically NOT 'lowest' volume)
4. Hold START and turn the power switch ON
5. Hold for about 5 seconds and release.. now wait for about 15 seconds (this is the joystick calibration procedure)
6. After a total of 20 seconds, turn off, put SD in, and boot up
7. You have analog volume control!

To disable, repeat the steps above again but disconnect the connector and it will detect it not there and revert to digital volume
</details>