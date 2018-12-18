# WiFi Troubleshooting
## Check for physical shorts on wifi module
When the back half of the case it put on, the USB connector can sometimes touch the WiFi module. This causes shorts and stops it working. The solution is to put a few layers of kapton tape over the wifi module, and to trim the legs of the USB connector on the back board.

## Connect using the wpa_supplicant.conf file
Due to keyboard and locale settings, it may be easier to create a text file with the wifi details in and load those in the wifi connection menu.

Insert SD into a PC, and create a file called `wpa_supplicant.conf` (warning, use Notepad++ or similar, normal notepad will not do, and may end up with a `.txt` extension, it must end in `.conf`) with the following contents:

```
country=US
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="My Cool Network"
    psk="my9a$$w0rd"
    key_mgmt=WPA-PSK
}
```

## Disabling WiFi completely
We can stop wifi loading COMPLETELY by editing `config.txt` and putting a `#` in front of the line, so that it looks like the following:

``` bash
#dtoverlay=sdio,poll_once=false
```

## Collecting the log file
For most debug related to crashes or wifi issues, the following log files are useful:

1. Plug in a USB keyboard
2. Press `F4` (to quit)
3. Run the command `sudo cp /var/log/messages /boot/messages.txt`
4. Run the command `sudo cp /var/log/syslog /boot/syslog.txt`
5. Power off
6. Put SD in PC, and upload the `messages.txt` and `syslog.txt` files that you see there

## Crashing or freezeing on boot? Most likely WiFi causing this
If it crashes or freezes on boot, try the above 'disable wifi' method followed by 'collecting the log file' and create an issue/email with the information

# LCD Troubleshooting
This section contains everything to do with the LCD.

## Banding on display
Inspect LCD ribbon cable connector for bridges, they are very difficult to spot:
[LCD Banding fix](https://youtu.be/HbeHoqdrTOg)

# Button Troubleshooting
## Mode button is always pressed
Put kapton tape on the USB C connector and the mode button pins, as they may come in to contact. Alternatively use snips/file to make the mode button legs flush with PCB.

# Power Troubleshooting
This section contains everything to do with main power (e.g. won't turn ON).

# USB Troubleshooting
This section contains everything to do with USB devices (e.g. the USB HUB, Arduino, USB Audio, External USB, etc).

# Software Troubleshooting
This section contains everything to do with the software (e.g. retropie) and maybe some general advice on where to look for help.