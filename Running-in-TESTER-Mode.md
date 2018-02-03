# Tester Mode
Tester mode allows for some basic automated tests to run to show the general system state of certain devices. It is a very basic test and show the USB devices attached and presents a colour-gradient test image to highlight any LCD defects. The tester mode was more designed for the older style boards where you had to solder everything by hand, but it might still be useful here!

## Enabling TESTER mode
1. Download the latest .zip for your board of choice from the 'releases' tab
2. Unzip, and using win32DiskImager to write it to SD
3. Open the SD in your computer and edit 'config-cs.txt' with "NOTEPAD++" (NOT the normal notepad)
4. Un-comment the 'TESTER' line, and the comment the 'NORMAL' line with a # so that it looks like:
```
#MODE=NORMAL
MODE=TESTER
#MODE=SHELL
```
5. Place SD in pi, power on, you're now in tester mode.. NOTE that in tester mode, the power switch will NOT power the Pi off! Instead it shows on the screen 'GPIO SHDN [ ON ]' (or [ OFF ]) to tell you what the Pi sees (ON = stay on, OFF = do a shutdown) .. you can slide the switch OFF and then press the mode button to kill it.
6. When testing done, reverse the steps in step 4 so that it now looks like this:
```
MODE=NORMAL
#MODE=TESTER
#MODE=SHELL
```