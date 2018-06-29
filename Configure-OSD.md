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

