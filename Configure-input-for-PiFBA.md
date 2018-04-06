### Config files
In order to get the _SAIO/Circuit-Sword_ controls to work with [PiFBA](https://github.com/RetroPie/pifba) a config file needs to be tweaked using the following command:  
`sudo nano /opt/retropie/configs/fba/fba2x.cfg`

Once in the editor pasting the following line will configure the buttons in the [Neo Geo CD gamepad](https://i.ytimg.com/vi/F7ADjv3zdlA/maxresdefault.jpg) layout.  
Be sure to remove the same lines in the **Joystick section** (_not_ the keyboard one) of your fba2x.cfg when you paste this:    
`[Joystick]`  
`# Get codes from "jstest /dev/input/js0"`  
`# from package "joystick"`  
`# Neo Geo CD layout for Kite's SuperAIO`  
`A_1=1`  
`B_1=2`  
`X_1=0`  
`Y_1=3`  
`L_1=6`  
`R_1=8`  
`START_1=4`  
`SELECT_1=5`  

Save with:  
_Controll + X_, then _Y_, then _Enter_

***
Alternatively you can change the mapping in a any way you prefer.  
Use this command to check your button numbers and tweak fba2x.cfg accordingly:  
`sudo jstest /dev/input/js0`