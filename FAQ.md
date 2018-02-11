# Frequently Asked Questions

### Q: Question
A: Answer

***
### Q: When will the next preorder open ?
A: Get notified by filling this form https://goo.gl/forms/e97uUvPOfUxPWdz82

***
### Q: How will the new-style Volume Control function now that the dial has been taken out?
A: The volume control is handled by the ATMEGA, and is adjusted using a [button combo](https://github.com/kiteretro/Circuit-Sword/wiki/Mode-Button-Shortcut-Keys). The ATMEGA stores the volume level and the Pi reads this data back and applies it to the OS volume level. There is a slight delay in updating the volume.

***
### Q: Can I use a USB A to C cable to transfer data from my pc to the gameboy? Can any data transfer over that port.
A: You would use WIFI to transfer things over, the USB allows for uploading code to arduino, or for flashing the SD card (but you could just take the SD card out and do it like that). It's the same as the Pi Zero where plugging in the USB doesn't allow data transfer but you use wifi instead

***
### Q: How's the battery usage with the CM3 compared to a Pi Zero ? 
A: Because all the regulators are mine (the compute module has no regulators of it's own (other than internal CPU ones)) it's actually pretty efficient! On max load and full brightness/wifi/volume/etc it will draw 500mA, on idle it will draw about 250-300mA (@4.2V)

***
### Q: Will the cutout for the new USB C port have to be any different in position or size from the one for the old board?
A: The USB C is in the same place as the micro, it is marginally wider than the Micro, when I put it in cases that i had previously made i just had to trim 0.5-1mm from one side to get it to fit.. because it's more "square" it actually fits better.. also one minor thing is that it pokes out further so to fit it you HAVE to make the cutout.. the good news is that any USB C cable will fit, unlike previously you had to use a 7mm long micro one!

***
### Q: can i use the game Boy with custom SD card reader game cartridge
A: I haven't designed it for that, not going to get too much into it but there are a whole host of issues with the cart slot SD so i've stayed away from it and to date haven't had a single SD issue. If you did want something in the cartridge slot, then get a USB to SD adapter, and wire it to the free USB port on the board. You could also do this with a full sized USB port and have a memory stick inside the cartridge.

***
### Q: do i really have to oreder the small fan as well? 
A: It's not compulsory, you should really put a heatsink on 100% though to slow down the heat build up.. generally you should plan for the CPU to get quite hot especially seeing as it is enclosed in a case.. the Pi will downclock when it hits 80*C i think, so worst case performance will slow down and games may become really slow.. if you can find another fan or a huuuge heatsink then by all means go for it! :D It is a Pi3 afterall and if you have used a Pi3 you'll know that it can get quite toasty! I would recommend the fan.

***
### Q: Will the board work with the custom 5500mAh battery in this forum ?
A: Yes it will. Without problem

***
### Q: Digital Volume Control Alternative?
A: You may have noticed a blank component on the board.. this as actually connected to the C1/C2 buttons (th 5th and 6th front buttons) and there is a mode in the arduino code to change these to be VOLUP/VOLDOWN.. you can either solder some wires from them and place your own buttons, or you can solder a rocker switch in this position, cut a hole in the case, and bring back a kind of volume control. See the page [here](https://github.com/kiteretro/Circuit-Sword/wiki/Digital-Volume-Guide) for details.

***
### Q: I want analog volume control back
A: Next pre-order will have an optional back board which will allow this. Check the latest pre-order.

***
### Q: Where can i put the joystick ? Can i put it on the left bottom part of the shell ?
A: The SAIO had a great big audio chip where on the front, the Circuit Sword has moved all this to the other side of the board.. the issue with SAIO is that you won't be able to fit the joystick there ! the CSO does away with all the completely and you can literally put it anywhere as there is next to nothing on that side of the board!

***
### Q: I want 2x joysticks
A: Do you really need 2x? Personally I don't think so but it's up to you!

***
### Q: Can i use HoolyHoo's screen brackets with the 640x480 screen ? (sold as an option)
A: Hoolyhoo’s original bracket won’t work for the 640x480 screen. You will have no room left and right to lower the bracket and make it sit. However he or other members on the forum may have a compatible bracket.

***
### Q: what are the outer and inner dimensions of the 640x480 screen?
A: read here https://github.com/kiteretro/Super-AIO/wiki/640x480-LCD-Build-Notes#size

***
### Q: Which screen bracket should i use with the 640x480 screen
A: read here https://www.sudomod.com/forum/viewtopic.php?p=47651#p47651

***
