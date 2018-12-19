# Technical Frequently Asked Questions

***
### Q: How will the new-style Volume Control function now that the dial has been taken out?
A: The volume control is handled by the ATMEGA, and is adjusted using a [button combo](https://github.com/kiteretro/Circuit-Sword/wiki/Mode-Button-Shortcut-Keys). The ATMEGA stores the volume level and the Pi reads this data back and applies it to the OS volume level. There is a slight delay in updating the volume.

***
### Q: Can I use a USB A to C cable to transfer data from my PC to the Circuit Sword? Can any data transfer over that port?
A: You would use WiFi to transfer things over. The USB allows for uploading code to Arduino or for flashing the SD card (but you could just take the SD card out and do it like that). It's the same as the Pi Zero where plugging in the USB doesn't allow data transfer but you use WiFi instead.

***
### Q: How's the battery usage with the CM3 compared to a Pi Zero? 
A: Because all the regulators are mine (the compute module has no regulators of its own other than internal CPU ones) it's actually pretty efficient! On max load and full brightness/WiFi/volume/etc it will draw 500mA. On idle it will draw about 250-300mA (@4.2V).

***
### Q: Will the cut-out for the new USB C port have to be any different in position or size from the one for the old board?
A: The USB C is in the same place as the Micro. It is marginally wider than the Micro. When I put it in cases that I had previously made I just had to trim 0.5-1mm from one side to get it to fit.. because it's more "square" it actually fits better.. also, one minor thing is that it pokes out further so to fit it you HAVE to make the cut-out.. the good news is that any USB C cable will fit, unlike previously when you had to use a 7mm long micro one!

***
### Q: Can I use the Circuit Sword with custom SD card reader?
A: I haven't designed it for that. I'm not going to go into it too much but there are a whole host of issues with the cart slot SD so I've stayed away from it and to date haven't had a single SD issue. If you did want something in the cartridge slot, then get a USB to SD adapter and wire it to the free USB port on the board. You could also do this with a full-sized USB port and have a memory stick inside the cartridge.

***
### Q: Do I really have to order the small fan as well? 
A: It's not compulsory, but you should really put a heatsink on 100% to slow down the heat build-up.. generally you should plan for the CPU to get quite hot especially seeing as it is enclosed in a case.. the Pi will downclock when it hits around 80*C, so worst case scenario the system may become really slow.. if you can find another fan or a huge heatsink then by all means go for it. It is a Pi3 after all and if you have used a Pi3 you'll know that it can get quite toasty! I would recommend the fan.

***
### Q: Will the board work with the custom 5500mAh battery from the forum?
A: Yes it will. Without any problems.

***
### Q: Digital Volume Control Alternative?
A: You may have noticed a blank component on the board.. this is actually connected to the C1/C2 buttons (the 5th and 6th front buttons) and there is a mode in the Arduino code to change these to be VOLUP/VOLDOWN.. you can either solder some wires from them and place your own buttons, or you can solder a rocker switch in this position, cut a hole in the case, and bring back a kind of volume control. See the page [here](https://github.com/kiteretro/Circuit-Sword/wiki/Digital-Volume-Guide) for details.

***
### Q: I want analog volume control back!
A: Next pre-order will have an optional back board which will allow this. Check the latest pre-order.

***
### Q: Where can I put the joystick? Can I put it on the left bottom part of the shell?
A: The SAIO had a great big audio chip there on the front! The Circuit Sword has moved all this to the other side of the board.. the issue with SAIO is that you won't be able to fit the joystick there! The Circuit Sword does away with all that completely and you can literally put it anywhere as there is next to nothing on that side of the board!

***
### Q: I want 2x joysticks!
A: Do you really need 2x? Personally I don't think so but it's up to you. The board supports 2x joysticks.

***
### Q: Can I use HoolyHoo's screen brackets with the 640x480 screen?
A: Hoolyhoo’s original bracket won’t work for the 640x480 screen. You will have no room left and right to lower the bracket and make it sit. However he or other members on the forum may have a compatible bracket.

***
### Q: What are the outer and inner dimensions of the 640x480 screen?
A: Read here: https://github.com/kiteretro/Super-AIO/wiki/640x480-LCD-Build-Notes#size

***
### Q: Which screen bracket should I use with the 640x480 screen?
A: Read here: https://www.sudomod.com/forum/viewtopic.php?p=47651#p47651

***
### Q: I don't want the 320 screen but just the 640 one!
A: The whole kit is sold with a 320 screen. If you order a 640 one, you will have a spare 320.

***
### Q: What can you say about sound?
A: The audio at the jack is STEREO, the AMP is MONO only (the VERY first SAIO had a stereo amp but went End of Life (EOL) after I prototyped with it.. The AMP before it gets fed has an audio summing circuit that converts the stereo to mono (to then go to the amp).. this all happens after the headphone jack, allowing stereo jack and mono amp! SO if you want stereo amp, you'll need to bring your own amp and unsolder some stuff.

***
### Q: Is it possible to turn the screen all the way on or off through hardware? Could I fake a sleep mode? 
A: The minimum brightness is set on the Arduino, so it is possible to set it to "off" by editing the code. The Pi does not have a sleep state, so will always be consuming a large amount of power when on.

***
### Q: Is it possible to have a full HD output from HDMI or just mirroring (cloning)? 
A: Maybe if someone wants to spend more time with it! At the moment it mirrors 320x240 to HDMI. You COULD change it so that it outputs 1080P to HDMI and then MIRRORS that down to 320x240 however that will have a fairly large performance hit... I'm making some menu options to enable "one time reboot to HDMI" which will go to HDMI for the next boot only (the next boot will be to internal screen) so it kind of will do that. It's all software stuff, so even if not available right now it's just a software update away!

***
### Q: Are you also giving the cable option for the joystick in the kit?
A: Yes, I will include 2x 4pin cables with it.

***
### Q: What bit depth is the LCD?
A: The LCD is configured to 18bit depth. As an FYI the Pi is default configured to output 16bit colour so there is currently no loss in colour information.

***
### Q: Do you know roughly how much space there is between the CPU of the CM3L and the back case of the shell?
A: In the front half of the shell, the CM3 protrudes 2.5mm above the LIP/EDGE of the shell. In the back half of the shell there is 8.5mm from the LIP/EDGE of the shell to the 'shelf' where the cartridge is. So that means you have ~6mm of height above the CM with keeping the cart shelf and a cart inside there. A 5mm heatsink is cutting it close but according to my measurements it will fit nicely.

***
### Q: What about the CM3Lite's own second SD card, is that exposed on your board in any way?
A:  The "second SD interface" is already used by the WiFi chip on the board (it's called SDIO, and works for SDs and also a lot of WiFi adaptors) so that cannot be used. What I have done is made solder pads available for the "unused USB port" of the built-in HUB that you could use for ANYTHING!

***
### Q: Just wondering if you have broken out any additional GPIO also?
A:  There is I2C available on the Arduino and 1 extra GPIO on the Arduino. There are 4x analog pins (on the joystick connectors) that could be used for anything. ALSO on the Pi itself, there are a number of GPIO that I have broken out into 0.1" headers! I've broken out EVERY SINGLE GPIO on the compute module (there aren't any that are left unconnected) and also labelled them with their Pi type function so that should make things easy. There are 10x GPIOs you can do whatever you like with. I have some ideas what to do with some of them for future project mods.. the entire SPI bus is available there so technically you could get a TFT screen connected up! Also, I2C is there so you're spoilt for interfaces!

***
### Q: Is there enough room to place copper shims on the chips underneath the CM3?
A: No, the chips UNDER the CM3 don't need a heatsink, the top one does though which the CPU and the one that actually makes heat.

***
### Q: Are the LEDs going to be snap off?
A: LEDs are no longer snap off, that's a good point though and there is JUST enough time to squeeze those in as solder pads.. you don't need to remove them (I'd advise you to keep them there) but I'll add solder pads for you.

***
### Q: What do you use to stick the fan to the Pi?
A: I use some 3M double-sided foam tape, and make little squares with 2x stuck on top of each other. Hint: don't make the squares very big, the tape is SUPER sticky and is hard to get off if you put on too much!

***
### Q: Next batch, are you going through a new design overhaul?
A: Changes to design will be mentioned on the pre-order page. Currently no major updates are planned.

***
### Q: How can I set up WiFi without a keyboard attached to the board?
A: Follow this guide from user YaYa: https://www.sudomod.com/forum/viewtopic.php?t=3567&view=unread#unread

***
### Q: I can't find the answer I'm looking for! How do I contact you?
A: Email: kite@kitesitemshop.com