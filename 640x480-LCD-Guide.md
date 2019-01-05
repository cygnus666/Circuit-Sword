# How to install the 640x480 LCD
This guide will show you everything that you need to know about the 640x480 upgraded LCD.

[[images/CSO/640LCD/PREVIEW.jpg]]

## Comparison with 320x240 display

### Benefits
* Higher resolution
* Better app scaling up

### Disadvantages
* Harder to fit (it's physically too wide)
* Harder to add supports to
* Lower overall brightness
* Lower vibrancy
* Software doesn't actually run higher than 320x240, only menus would be clearer (although scaling would make any in-between resolutions look nicer)

## Size
Here are the physical dimensions of the LCD:

[[images/CSO/640LCD/SPECS.png]]

## Software
The Arduino does NOT need re-programming, it comes already with the 640x480 LCD enabled. The only change needed is to the raspberry pi `config.txt` to set the resolution higher.

1. Insert SD into your PC (after it has been imaged)
2. Open up the visible partition and open `config.txt` with Notepad++ (do not use a regular text editor)
3. Scroll to the very bottom and "comment out" the 320x240 bits (this means adding a # to the start of each line) and "uncomment" the 640x480 bits (this means removing the # at the start of each line) so that it looks like:

_640x480 LCD is enabled in the following image_
[[images/CSO/640LCD/PI_640LCD1.png]]

### Overscan settings
These settings are NOT PERFECT but get the job done.. add these values to the END of `/boot/config.txt`. Adjust the numbers depending on how it fits, the numbers below worked ok for me.

KNOWN CAVEAT: This _scales_ the image down to fit, so there is slight blurring.. for this reason it is not 'pixel perfect'. I am working on a better pixel perfect scaling but it isn't ready yet..

``` bash
overscan_left=0
overscan_right=5
overscan_top=10
overscan_bottom=0
overscan_scale=1
```

## Hardware
## Enabling backlight boost
The 640x480 LCD needs more power to run at full brightness. On the Circuit Sword underneath the Compute Module is a solder jumped labelled "BL_BOOST". Solder over this to make a small bridge.

## Prepare LCD
We need to make the biggest edge of the LCD as slim as possible, and we can modify the LCD itself and trim some of the WHITE plastic and also the METAL SHELL. Start by removing the outer metal shell. This is done by slowly unclipping the edge clips and levering out: 

[[images/CSO/640LCD/5.jpg]]

Trim the top edges with a sharp knife VERY CAREFULLY. DO NOT CUT INTO THE BLACK STUFF AT ALL, IT WILL DAMAGE THE LCD.

[[images/CSO/640LCD/6.jpg]]

More trimming:

[[images/CSO/640LCD/7.jpg]]

These are the bits that we are specifically targeting, and the WHITE ONLY:

[[images/CSO/640LCD/8.jpg]]

Trim the metal shell with a cutting disk. you could choose to not put the metal shell back on at all! It may lower the brightness as the inside metal is used for reflective gains:

[[images/CSO/640LCD/9.jpg]]

## Fit LCD
Connect up the adapter. When it goes inside the case it will be folded as shown in the image below:

[[images/CSO/640LCD/10.jpg]]

It is a good idea to cover the back of the LCD and ALSO the adapter in kapton tape to prevent shorting.
Using epoxy is the best way to fit and secure the screen.

## Font Size

By default, CSO [sets a small console font size](https://github.com/kiteretro/Circuit-Sword/blob/master/settings/config-cs.txt#L18) at startup.  This is difficult to read with the 640x480 screen.
To use the default system defined font, comment out the `STARTUPEXEC` line in `/boot/config-cs.txt`.