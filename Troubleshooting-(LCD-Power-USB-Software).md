# WiFi Troubleshooting
## Check for physical shorts on wifi module
When the back half of the case it put on, the USB connector can sometimes touch the WiFi module. This causes shorts and stops it working. The solution is to put a few layers of kapton tape over the wifi module, and to trim the legs of the USB connector on the back board.

## Disabling WiFi completely
We can stop wifi loading COMPLETELY by editing `config.txt` and putting a `#` in front of the line, so that it looks like the following:

``` bash
#dtoverlay=sdio,poll_once=false
```

## Collecting the log file
For most debug related to crashes, the /var/log/messages file is useful. This can be collected by doing:

1. Plug in a USB keyboard
2. Press `F4` (to quit emulationstation)
3. Run the command `sudo cp /var/log/messages /boot/messages.txt`
4. Power off
5. Put SD in PC, and upload the `messages.txt` file you see there

## Crashing or freezeing on boot? Most likely WiFi causing this
If it crashes or freezes on boot, try the above 'disable wifi' method followed by 'collecting the log file' and create an issue/email with the information

# LCD Troubleshooting
This section contains everything to do with the LCD.

# Button Troubleshooting
## Mode button is always pressed
Put kapton tape on the USB C connector and the mode button pins, as they may come in to contact. Alternatively use snips/files to make the mode button legs not so long.

# Power Troubleshooting
This section contains everything to do with main power (e.g. won't turn ON).

# USB Troubleshooting
This section contains everything to do with USB devices (e.g. the USB HUB, Arduino, USB Audio, External USB, etc).

# Software Troubleshooting
This section contains everything to do with the software (e.g. retropie) and maybe some general advice on where to look for help.