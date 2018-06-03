# Overview
As of the software release v1.2.0, there is a new script in the `Circuit-Sword` directory that allows the following:

* Calibrate joystick
* Enable/disable joystick 1 or 2
* Invert the axis of joystick 1 or 2
* Enable/disable analog volume
* Show status report

# Update Arduino code
If you are using the Circuit-Sword with hardware revision V1.1E, you will need to update the arduino code. If you are running 1.2A or above, no update needed.

# Running
Enable SSH, and SSH in to the Circuit-Sword (raspberry pi) and run the following:

1. Stop the battery monitor running:
``` shell
sudo service cs-osd stop
```

2. Run the configuration:
``` shell
python Circuit-Sword/cs-configure.py
```

3. When finished configuring, re-enable the battery monitor:
``` shell
sudo service cs-osd start
```

# Using the configurator
When launched, you will be presented with the following information:
``` shell
pi@retropie:~ $ python Circuit-Sword/cs-configure.py
INFO:root:Program Started

GENERAL INFORMATION
Mode pressed: 0
Wifi enabled: 1
Backlight:    100%

VOLUME INFORMATION
Amp enabled:            1
Current volume:         50%
Analog volume enabled:  0
Analog volume adc:      0

JOYSTICK INFORMATION
JOY 1 enabled: 0 - (X: 901 Y:0)
  JOY 1 X invert: 1
  JOY 1 Y invert: 0
JOY 2 enabled: 0 - (X: 908 Y:0)
  JOY 2 X invert: 1
  JOY 2 Y invert: 0

MAIN MENU
---------
1 - Joystick calibration
2 - Invert JOY 1 X config
3 - Invert JOY 1 Y config
4 - Invert JOY 2 X config
5 - Invert JOY 2 Y config
6 - Toggle JOY 1 enabled config
7 - Toggle JOY 2 enabled config
8 - Toggle Analog Volume enabled config
ENTER - Refresh information
X - Quit

Enter selection followed by ENTER:

```

## Usage
Press the corresponding key (e.g. "1") followed by the RETURN/ENTER key to execute. On screen messages will instruct on what to do next. You can press RETURN/ENTER on its own to refresh the screen to update the information shown.

## Description of information
### GENERAL INFORMATION
* `Mode pressed: 0` Is the mode button currently pressed? Useful to debug if mode button is functional.
* `Wifi enabled: 1` Is wifi meant to be abled? Regardless of whether it is or not, this is the desired state.
* `Backlight:    100%` The backlight brightness in % 

### VOLUME INFORMATION
* `Amp enabled:            1` Is the audio amplifier to speaker enabled?
* `Current volume:         50%` The current volume in % as read from the arudino (digital volume or analog)
* `Analog volume enabled:  0` Is the analog volume pot enabled for use?
* `Analog volume adc:      0` What is the RAW ADC value for the analog volume pot?

### JOYSTICK INFORMATION
The joystick is enabled by performing a calibration. The values shown below are useful for debugging that your joystick is connected and working properly. E.g. you can move the joystick, press the ENTER key to refresh the data, and check which value changes.
* `JOY 1 enabled: 0 - (X: 901 Y:0)` Is JOY1 Enabled? Also it's raw mapped values (inverts applied)
* `  JOY 1 X invert: 1` Is JOY1 X axis inverted?
* `  JOY 1 Y invert: 0` Is JOY1 Y axis inverted?
* `JOY 2 enabled: 0 - (X: 908 Y:0)` Is JOY2 Enabled? Also it's raw mapped values (inverts applied)
* `  JOY 2 X invert: 1` Is JOY2 X axis inverted?
* `  JOY 2 Y invert: 0` Is JOY2 Y axis inverted?