# Tester Mode
Tester mode allows for some basic automated tests to run to show the general system state of certain devices. It is a very basic test and show the USB devices attached and presents a colour-gradient test image to highlight any LCD defects. The tester mode was more designed for the older style boards where you had to solder everything by hand, but it might still be useful here!

## Enabling TESTER mode
1. Open the SD in your computer and edit 'config-cs.txt' with "NOTEPAD++" (NOT the normal notepad)
2. Un-comment the 'TESTER' line, and then comment the 'NORMAL' line with a # so that it looks like:
``` bash
#MODE=NORMAL
MODE=TESTER
#MODE=SHELL
```
3. Place SD in pi, power on, you're now in tester mode.. NOTE that in tester mode, the power switch will NOT power the Pi off! Instead it shows on the screen 'GPIO SHDN [ ON ]' (or [ OFF ]) to tell you what the Pi sees (ON = stay on, OFF = do a shutdown) .. you can slide the switch OFF and then press the mode button to kill it.
4. When testing done, reverse the steps in step 4 so that it now looks like this:
``` bash
MODE=NORMAL
#MODE=TESTER
#MODE=SHELL
```