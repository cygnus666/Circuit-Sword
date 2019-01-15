_Click_ ⯈ _to expand_
1. Plug a USB C cable into the Circuit Sword and check that the "PG" LED comes on

2. Hold down the "power" button and check that the status LEDs come on

3. Unplug the USB C cable then plug in the battery (WARNING: USING A CONNECTOR WITH THE WRONG PIN-OUT WILL BREAK THE CIRCUIT SWORD)

4. Hold down the "power" button and check that the status LEDs come on

5. Plug in the USB C cable and check that the "CHRG" and "PG" LEDs come on

6. Unplug the USB C cable and battery, then plug in the Add-on board and power switch board (NOTE: INSERT THE FPC CABLE BLUE-SIDE UP). Check that the power switch is "OFF"

7. Plug in the battery then the USB C cable. Turn the power switch "ON" and check that the status LEDs come on

8. Cover the Wi-Fi module using 3 layers of Kapton tape

9. Insert the Raspberry Pi Compute Module 3 Lite at a 45° angle then carefully click it into place

10. Plug in the LCD

11. Download the [Circuit Sword Software](https://github.com/kiteretro/Circuit-Sword/releases) then use Win32 Disk Imager to write it to an SD card. Open the `config-cs.txt` file using "Notepad++" then change `#MODE=TESTER` to `MODE=TESTER`

12. Insert the SD card then turn the power switch "ON". Once fully booted check that all of the tests have passed

13. Hold down the "mode" button and wait for the configuration menu to appear

14. Turn the power switch "OFF" and wait for the Circuit Sword to shut down

15. Solder an additional "mode" button to the power switch board then trim the pins

16. Solder the spacers to the Add-on board one on top of the other

17. Stick the heatsink to the Raspberry Pi Compute Module 3 Lite

18. Stick the fan to the Raspberry Pi Compute Module 3 Lite using double-sided foam tape

19. Solder the 2-pin cable to the speaker then plug in the speaker