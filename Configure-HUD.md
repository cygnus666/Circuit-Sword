# Configuration for CS-HUD (v1.3.0 and above)

## Hiding the battery icon
It is possible to hide the battery icon from view and have it only appear when the battery is low. The MODE button menu and everything else still functions as expected.

1. Enable wifi and ssh
2. SSH in to the Circuit Sword
3. Edit the service file and add ` -s` to the service by doing the following:

`sudo vim.tiny /lib/systemd/system/cs-hud.service`

Then add the ` -s` so that it looks like:

```
ExecStart=/home/pi/Circuit-Sword/cs-hud/cs-hud -s
```

_Hint: Press `i` to enter text mode, when done editing text press `ESC` key, then `:` and then `wq` and then `ENTER` key. Or use `nano` instead of `vim.tiny` if you are more familiar with that_

4. Run the command `sudo systemctl daemon-reload`
5. Run the command `sudo systemctl restart cs-hud.service`

To undo, follow the same steps but _remove_ the `-s` instead. Also note that if you perform an `./update.sh` it will undo this change. In future this will be a toggle feature with an easy way to set it and when available this page will be updated.

# Configuration for CS-OSD (v1.2.1 and below)

_Note that this only applies to versions running the `cs-osd` service. If you are running the `cs-hud` service (where there is a menu pop up when you hold the MODE button) then these currently do not apply and will come in a future update_
### Move around icons

In a default setup the OSD icons sit right at the extreme edge of the screen, which may cause them to sit outside the border of your display lens, easy to fix.

Mount your SD card via USB or connect via SSH and edit the following file in the retropie partition:

`/home/pi/Circuit-Sword/cs-osd/cs-osd/config.ini`

Adjust the lines referencing x or y coordinates to suit your configuration.

A safe configuration would be:

`batt_x    = 33                ; X position of battery icon`

`batt_y    = 6                  ; Y position of battery icon`


`wifi_x    = 49                ; X position of wifi icon`

`wifi_y    = 6                  ; Y position of wifi icon`


`mute_x    = 65                ; X position of mute icon`

`mute_y    = 6                  ; Y position of mute icon`

