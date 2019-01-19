_Click_ ⯈ _to expand_

## How do I force the Circuit Sword to shut down?
Turn the power switch "OFF" then press the "mode" button

## How do I install Circuit Sword Software updates?
1. Enable SSH and check that the Circuit Sword is connected to Wi-Fi then log in to the Raspberry Pi Compute Module 3 Lite using SSH
2. Run the command `cd Circuit-Sword` then run the command `sudo ./update.sh`

## How do I connect to Wi-Fi without typing out a password?
Insert your Circuit Sword SD card into a PC then create a file called `wpa_supplicant.conf` using “Notepad++” that contains the text below (insert your own country, ssid and psk)
```
country=US
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="My Network Name"
    psk="mypassword"
    key_mgmt=WPA-PSK
}
```

## How do I hide the battery icon?
1. Enable SSH and check that the Circuit Sword is connected to Wi-Fi then log in to the Raspberry Pi Compute Module 3 Lite using SSH
2. Open the file `/lib/systemd/system/cs-hud.service` by running the command `sudo nano /lib/systemd/system/cs-hud.service` then change ‘ExecStart=/home/pi/Circuit-Sword/cs-hud/cs-hud’ to ‘ExecStart=/home/pi/Circuit-Sword/cs-hud/cs-hud -s’
3. Press `CTRL` and `X` then press `ENTER` to save
4. Run the command `sudo reboot`

## How do I enable the volume wheel?
1. Plug in the alternative Add-on board then plug in the volume wheel’s 3-pin cable
2. Enable SSH and check that the Circuit Sword is connected to Wi-Fi then log in to the Raspberry Pi Compute Module 3 Lite using SSH
3. Run the command `sudo service cs-hud stop` then run the command `python Circuit-Sword/cs-configure.py`
4. Press `8` then press `ENTER`
5. Press `ENTER` again then check that the command output reads `Analog volume enabled:  1`
6. Press `X` then press `ENTER`
7. Run the command `sudo service cs-hud start`

## How do I enable the 640x480 LCD?
1. Solder a bridge between the solder pads labelled below
2. Insert your Circuit Sword SD card into a PC then open the file `config.txt` using "Notepad++". Add and remove `#` as follows
```
# Enable 320x240 custom display mode
#framebuffer_width=320
#framebuffer_height=240
#display_rotate=2
#dpi_output_format=24597
#hdmi_timings=320 1 20 30 38 240 1 4 3 10 0 0 0 60 0 9600000 1

# Enable 640x480 custom display mode
framebuffer_width=640
framebuffer_height=480
display_rotate=3
dpi_output_format=287269
hdmi_timings=480 1 5 5 14 640 1 3 3 3 0 0 0 60 0 32000000 1
```

## How do I enable joysticks?
1. Enable SSH and check that the Circuit Sword is connected to Wi-Fi then log in to the Raspberry Pi Compute Module 3 Lite using SSH
2. Run the command `sudo service cs-hud stop` then run the command `python Circuit-Sword/cs-configure.py`
3. Press `1` then press `ENTER`. Slowly rotate the joystick(s) until calibration is complete
4. Press `ENTER` then check that the command output reads `JOY 1 enabled: 1`
5. Press `X` then press `ENTER`
6. Run the command `sudo service cs-hud start`

## How do I add more status LEDs?
Use the solder pads labelled below (circuit diagram provided)

## How do I reprogram the microcontroller?
1. Enable SSH and check that the Circuit Sword is connected to Wi-Fi then log in to the Raspberry Pi Compute Module 3 Lite using SSH
2. Run the command `sudo service cs-hud stop` then run the command `cd Circuit-Sword`
3. Run the command `sudo ./flash-arduino.sh`
4. Run the command `sudo reboot`

## Can’t find the answer you’re looking for?
Check out the [support forum](https://www.sudomod.com/forum/viewforum.php?f=51) or e-mail kite@kitesitemshop.com