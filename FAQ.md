# Frequently Asked Questions

### Q: When will the next pre-order open?
A: To receive all the latest updates follow me on Instagram ([@kiteretro](https://www.instagram.com/kiteretro/)) or join my [mailing list](https://goo.gl/forms/e97uUvPOfUxPWdz82). Both will get notifications of upcoming pre-orders for the Circuit Sword, or any other products (e.g. VMU).

***
### Q: How much will it cost?
A: When the pre-order is opened, the individual item cost will be shown

***
### Q: Do you ship to .. ?
A: Shipping is calculated at checkout, PayPal doesn't implement a nice set of shipping options (but only if you have a US seller account, go figure..) so prices are set at an international rate! Sorry UK people but I have to charge the full amount, refunds aren't possible due to time (they will arrive next day after posting tho!). ALL shipments are sent first class tracked by RoyalMail and will require a signature. Tracking information will make its way to you once shipped!

Shipping **only** to **the United Kingdom, the United States, Canada, Europe, Australlia, New Zealand, Brazil** and **Japan**. (You will get a refund if you are not in one of these zones).

If you have any special postage requirements, please include in the order notes.

***
### Q: How does ordering work? I've changed my mind!
A: Payment is by PayPal, I have used the 'add to cart' functionality and when you click the buttons above it will take you to a PayPal cart (you can keep adding things to the cart if you come back to this page, I suggest 'right click -> open in a new tab/window'). PayPal offers full buyer protection, any issues please get in contact with me first!

PLEASE SET YOUR ADDRESS CORRECTLY! You will be charged if re-shipment is required due to incorrect address, so get it right :) If you change your address please email me but please try to plan ahead where possible! It is very time consuming having to change individual order addresses.. If you request an address change after the order has been packed, you will need to re-pay for postage. If the order has already been sent out, it is your responsibility to track and collect the items. If the parcel is returned to me you will need to re-pay for postage. If it does not return it is your responsibility to follow up with the mail carrier.

Full refunds on all pre-orders cancelled before pre-orders close. cancellations made after pre-orders close will not be processed.

All items are tested to ensure that they are in good working condition before they are shipped, but should your item arrive damaged or faulty please contact (email) within 30 days to request a replacement/repair.

***
### Q: How will the new-style Volume Control function now that the dial has been taken out?
A: The volume control is handled by the ATMEGA, and is adjusted using a [button combo](https://github.com/kiteretro/Circuit-Sword/wiki/Mode-Button-Shortcut-Keys). The ATMEGA stores the volume level and the Pi reads this data back and applies it to the OS volume level. There is a slight delay in updating the volume.

***
### Q: Can I use a USB A to C cable to transfer data from my PC to the Game Boy? Can any data transfer over that port?
A: You would use WiFi to transfer things over. The USB allows for uploading code to Arduino or for flashing the SD card (but you could just take the SD card out and do it like that). It's the same as the Pi Zero where plugging in the USB doesn't allow data transfer but you use WiFi instead.

***
### Q: How's the battery usage with the CM3 compared to a Pi Zero? 
A: Because all the regulators are mine (the compute module has no regulators of its own other than internal CPU ones) it's actually pretty efficient! On max load and full brightness/WiFi/volume/etc it will draw 500mA. On idle it will draw about 250-300mA (@4.2V).

***
### Q: Will the cut-out for the new USB C port have to be any different in position or size from the one for the old board?
A: The USB C is in the same place as the Micro. It is marginally wider than the Micro. When I put it in cases that I had previously made I just had to trim 0.5-1mm from one side to get it to fit.. because it's more "square" it actually fits better.. also, one minor thing is that it pokes out further so to fit it you HAVE to make the cut-out.. the good news is that any USB C cable will fit, unlike previously when you had to use a 7mm long micro one!

***
### Q: Can I use the Game Boy with custom SD card reader game cartridge?
A: I haven't designed it for that. I'm not going to go into it too much but there are a whole host of issues with the cart slot SD so I've stayed away from it and to date haven't had a single SD issue. If you did want something in the cartridge slot, then get a USB to SD adapter and wire it to the free USB port on the board. You could also do this with a full-sized USB port and have a memory stick inside the cartridge.

***
### Q: Do I really have to order the small fan as well? 
A: It's not compulsory, but you should really put a heatsink on 100% to slow down the heat build-up.. generally you should plan for the CPU to get quite hot especially seeing as it is enclosed in a case.. the Pi will downclock when it hits 80*C I think, so worst case scenario performance will slow down and games may become really slow.. if you can find another fan or a huge heatsink then by all means go for it. It is a Pi3 after all and if you have used a Pi3 you'll know that it can get quite toasty! I would recommend the fan.

***
### Q: Will the board work with the custom 5500mAh battery in this forum?
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
A: Do you really need 2x? Personally I don't think so but it's up to you!

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
### Q: Can I order the 640x480 screen later?
A: 640 can be ordered later, just email me when you want one. Seeing as you have to glue and cut the case for either LCD you would need a NEW SHELL to do it, these things are permanently fixed in so it's probably best to get a new case.. which is easier (IMHO) than cutting out the old one.. the included 320x240 is great anyway, way easier to install and is brighter.. 640 is only an option as people kept requesting it :P still trying to find a better fitting one..

***
### Q: I don't want the 320 screen but just the 640 one!
A: The whole kit is sold with a 320 screen. If you order a 640 one, you will have a spare 320.

***
### Q: What can you say about sound?
A: The audio at the jack is STEREO, the AMP is MONO only (the VERY first SAIO had a stereo amp but went End of Life (EOL) after I prototyped with it.. The AMP before it gets fed has an audio summing circuit that converts the stereo to mono (to then go to the amp).. this all happens after the headphone jack, allowing stereo jack and mono amp! SO if you want stereo amp, you'll need to bring your own amp and unsolder some stuff.

***
### Q: Is it possible to turn the screen all the way on or off through hardware? Could I fake a sleep mode? 
A: The minimum brightness is set on the Arduino, so it is possible to set it to "off". You'll have to do some tests, because when on the home screen (emulation station) it uses a fair bit of CPU.. there may be a way to reduce it, and also downclock the CPU?

***
### Q: Is it possible to have a full HD output from HDMI or just mirroring (cloning)? 
A: Maybe if someone wants to spend more time with it! At the moment it mirrors 320x240 to HDMI. You COULD change it so that it outputs 1080P to HDMI and then MIRRORS that down to 320x240 however that will have a fairly large performance hit... I'm making some menu options to enable "one time reboot to HDMI" which will go to HDMI for the next boot only (the next boot will be to internal screen) so it kind of will do that. It's all software stuff, so even if not available right now it's just a software update away!

***
### Q: Are you also giving the cable option for the joystick in the kit?
A: Yes, I will include a 4pin cable with it.

***
### Q: Is the LCD included configured for 24-bit this time?
A: No, it's the same 18bit as before.

***
### Q: Do you know roughly how much space there is between the CPU of the CM3L and the back case of the shell?
A: In the front half of the shell, the CM3 protrudes 2.5mm above the LIP/EDGE of the shell. In the back half of the shell there is 8.5mm from the LIP/EDGE of the shell to the 'shelf' where the cartridge is. So that means you have ~6mm of height above the CM with keeping the cart shelf and a cart inside there. A 5mm heatsink is cutting it close but according to my measurements it will fit nicely.

***
### Q: What about the CM3Lite's own second SD thingy, is that exposed on your board in any way?
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
A: This is the first "overhaul" of the design (SAIO (PiZero/Pi3) to CSO (CM3)) and I have no plans to "overhaul" any time soon! I don't even know what I could possibly change to be honest! I do plan to continue my pattern of pre-orders.. I listen to feedback and if any improvements can be made between pre-orders I make those changes (e.g. the SAIO went from V0.5E1 (SMD solder) to V0.6C (through hole solder)) so any feedback will go into the designs! The only ADDITION I'm thinking of making in the future (next batch) would be an optional back board (which would be an optional extra for like £5 or so) that gives you back the analog volume control (volume wheel). This would be backwards compatible with the current version, I just won't have it ready in time for this current order.

***
### Q: How can I set up WiFi without a keyboard attached to the board?
A: Follow this guide from user YaYa: https://www.sudomod.com/forum/viewtopic.php?t=3567&view=unread#unread

***
### Q: I can't find the answer I'm looking for! How do I contact you?
A: Email: kite@kitesitemshop.com