# How to install the 640x480 LCD
This guide will show you everything that you need to know about the 640x480 upgraded LCD.

[[images/CSO/640LCD/PREVIEW.jpg]]

Here is a video of it in action: https://youtu.be/2dObgpBAJpc

## Comparison with 320x240 display
The following images show the 640x480 and the 320x240 side by side.
NOTE that in the pictures the 320x240 looks like it has black bands, you can't actually see them with human eyes but the camera picks them up. Also note that on the 640x480 I had accidentally put width scaling on so the character is stretched slightly..

[[images/CSO/640LCD/COMP1.jpg]]
[[images/CSO/640LCD/COMP2.jpg]]

### Benefits
* Higher resolution
* Better game scaling up

### Disadvantages
* Harder to fit (it's physically too wide)
* Harder to add supports to
* Lower overall brightness
* Lower vibrancy
* Games don't actually run higher than 320x240, only menus in retropie would be clearer

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

## Fitting the LCD
### Preparing case for LCD
Do the screen surround cut out as per normal steps in guide. It is a good idea to use a black marker to run on the inside edge of the cutout so when viewed at an angle you can't see the grey plastic.

[[images/CSO/640LCD/1.jpg]]

The 640x480 LCD is very slighly wider than the shell.. it is required that the inside of the case needs to be trimmed to allow it to fit, and also for proper alignment.

The only edge that needs indenting (for a better word) is the side with the CONTRAST slot. This is the side where the thick piece of metal on the LCD is closest to.

To make the indent, I used a rotary tool with the pink grinding attachment and VERY SLOWLY took away a layer at a time. I then used a small FLAT file (rectangular tip) to slide up and down the area to make it neater.

NOTE: Prepare the LCD first (see further steps) as you will need to keep placing it to make sure it fits. With the modifications to the LCD the middle of the indentation will require the most material removed. The top and bottom won't need so much removing.

[[images/CSO/640LCD/2.jpg]]

Keep filing and grinding it in iterations:

[[images/CSO/640LCD/3.jpg]]

If you hold it up to a light, you will be able to see light through it when the wall is getting thin. Do this often to avoid making holes in the side. You can see in the following image that I actually broke through the wall. From the outside it isn't noticable so I'm going to leave it as is. You could use some plastic filler:

[[images/CSO/640LCD/4.jpg]]

### Prepare LCD
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

### Fit LCD
Connect up the adapter. When it goes inside the case it will be folded as shown in the image below:

[[images/CSO/640LCD/10.jpg]]

It is a good idea to cover the back of the LCD and ALSO the adapter in kapton tape to prevent shorting.

If the trimmings have been done as per the previous steps, you should have a edge-less LCD viewing area as shown below:

NOTE: In this sample fitting I cut into the BLACK stuff when trimming the LCD.. as you can see on the RIGHT half of the LCD it is only showing every other pixel! You have been warned!

[[images/CSO/640LCD/11.jpg]]
