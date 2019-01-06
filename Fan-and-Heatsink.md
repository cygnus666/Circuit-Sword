# Fan and Heatsink Installation
It is generally a good idea to put a small heatsink on the Compute Module CPU to allow it to radiate heat as it will very slowly climb in temperature until it reaches a threshold which causes it to down clock (around 80C?). A heatsink will increase the heat radiation, and a fan will help force cooler air into it to actively cool it down.

## Heatsink
Depending on your heatsink, it may or may not come with double sided tape already. If it doesn't come with tape, it is advised to use regular double sided tape and apply it. Nothing special is required as the temperatures we are dealing with are very low (this isn't a high end CPU, it's a Raspberry Pi 3!).

Apply tape, and apply heatsink to CPU on the top. The other chips do not need cooling.

## Fan
Solder the fan to the FAN connector at the top of the board. This will turn the fan ON at 50-60C and turn it off when it falls below 5-10C of the set temperature. This is adjustable in the source code (see python source code).

If you have a board version V1.2A or above, it will have a built in fan connector.

To physically attach the fan, use a 3D printed bracket (find on forum) or a few layers of double sided foam tape.