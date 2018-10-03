# Mode Button
The 'MODE' button has a couple of uses:

1. When the power switch is ON, it enables "button combos" to do certain actions (see below)
2. When the power switch is OFF, while the Pi is running, pressing the mode button will insta-kill the power! This is useful specifically if the Pi freezes or crashes, and is a way to force a power down (alternative would be to remove the battery)

## Button Combos
* MODE + UP = VOL UP
* MODE + DOWN = VOL DOWN
* MODE + RIGHT = BACKLIGHT BRIGHTNESS UP
* MODE + LEFT = BACKLIGHT BRIGHTNESS DOWN
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

To set it up, first 'configure gamepad' from the main menu. Enter everything as normal but when you get to "JOYSTICK 2 UP" you must FIRST do the "MODE + R1" combo, and then press up/down/left/right to assign it to JOYSTICK2. Once done do "MODE + L1" to disable (as you won't be able to navigate menus using the DPAD without disabling the combo first).

Now when you are using it, do "MODE + R1" and now the DPAD will act as the the second joystick.

# New Style HUD
As of version [v1.3.0](https://github.com/kiteretro/Circuit-Sword/releases/tag/v1.3.0) there has been a much improved battery icon HUD implemented. The new HUD features a number of improvements:
* Faster update rate
* Helpful overlay shown when MODE button is held down (showing which keys do what and including useful stats)
* On screen keyboard (for entering wifi passwords or in menus where you need the 'ESC' key or something)
* When analog volume is used it will pop up at the top the volume percentage when changed

_Idle normal use_

[[images/CSO/HUD_IDLE.png]]

_MODE button held down_

[[images/CSO/HUD_MENU.png]]

_On screen keyboard enabled_

[[images/CSO/HUD_OSK.png]]

## On Screen Keyboard
The keyboard allows simple input by sending key presses. Use the DPAD to move the cursor and A to send. No other keys have been implemented yet.