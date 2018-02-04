# Mode Button
The 'MODE' button has a couple of uses:

1. When the power switch is ON, it enables "button combos" to do certain actions (see below)
2. When the power switch is OFF, while the Pi is running, pressing the mode button will insta-kill the power! This is useful specifically if the Pi freezes or crashes, and is a way to force a power down (alternative would be to remove the battery)

## Button Combos
* MODE + A = WIFI ENABLE
* MODE + B = WIFI DISABLE
* MODE + Y = AUDIO AMP OFF
* MODE + X = AUDIO AMP ON
* MODE + START = DEBUG INFO ON
* MODE + SELECT = DEBUG INFO OFF (power off will also reset this)
* MODE + R1 = DPAD is now a 2nd button input (rather than a HAT input)
* MODE + L1 = DPAD is reset to HAT input

## MODE + R1/L1 Usage
This button combo when activated will change the DPAD input from the 'HAT' to some other button inputs. What this means is that you can have the DPAD act like a joystick or just 'other input'.

For example, when playing N64 games and you only have 1x joystick installed on your creation.. the default retropie config has the JOYSTICK1 to be main joystick, the DPAD to but the DPAD, and JOYSTICK2 to be the 4x 'C' buttons, A,B,L1,R1 as they are, and R2 as Z. Most if not all N64 games never use the DPAD AND JOYSTICK at the same time, so on our example creation the DPAD is currently wasted.. "wouldn't it be great if I could use the DPAD as the C buttons" ? YES, and that is what this button combo allows you to do!

To set it up, first 'configure gamepad' from the main menu. Enter everything as normal but when you get to "JOYSTICK 2 UP" you must FIRST to the "MODE + R1" combo, and then press up/down/left/right to assign it to JOYSTICK2. Once done do "MODE + L1" to disable (as you won't be able to navigate menus using the DPAD without disabling the combo first.

Now whne you are in N64 game, do "MODE + R1" and now the DPAD will act as the C buttons! This applies to anything else that uses the 2nd joystick OR if you re-map in the emulator it could do anything that you wanted.