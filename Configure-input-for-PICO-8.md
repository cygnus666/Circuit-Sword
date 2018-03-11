## Setup the PICO-8 Fantasy Console
To run the [PICO-8 Fantasy Console ](https://www.lexaloffle.com/pico-8.php?page=faq) on your handheld device (_SAIO/Circuit-Sword_) you want download a couple of packages first.


### Purchase PICO-8 
Of course, you'll need to get the PICO-8 software. [Purchase a licence here](https://www.lexaloffle.com/pico-8.php#getpico8) and they will email you a key which you need to download the (_Raspberry Pi zip_) file on their site.

When downloaded unzip the packaged and copy it over to your Pi to the following path: `/home/pi/`. (The easiest way to do so is to plugin the SD card into your computer and look for the path mentioned above.)

### Config files
In order to get the _SAIO/Circuit-Sword_ controls to work some config files need to be tweaked. You can download a predefined setup [here](https://www.dropbox.com/s/sens82mm607xcsk/pico8filesforSAIO.zip?dl=1) ([mirror download](http://www.mediafire.com/file/xx6o0n5swte453d/pico8filesforSAIO.zip)). When downloaded unzip the packaged and copy the whole _.lexaloffle_ folder over to your Pi to the following path: `/home/pi/`

***
Alternatively you can map all core keys to the equivalent CSO game controller buttons manually. This can be done by editing the _sdl_controllers.txt_ file in _/home/pi/.lexaloffle_ folder:  
`nano /home/pi/.lexaloffle/pico-8/sdl_controllers.txt`

Once in the editor paste the following line:  
`03000000412300003680000001010000,Arduino LLC Arduino Leonardo,platform:Linux,x:b2,a:b1,b:b0,y:b3,back:b5,start:b4,dpleft:h0.8,dpdown:h0.4,dpright:h0.2,dpup:h0.1`

Save with:  
_Controll + X_, then _Y_, then _Enter_


### Required Libraries
PICO-8 requires the _libwiringPi.so_ libraries. You can get these [here](http://wiringpi.com/download-and-install) or simply install them on your Raspberry Pi via the following terminal command:

`sudo apt-get install wiringpi` 

(To access the terminal from _emulationstation_ plugin a keyboard and press _F4_. To get back to emulationstation simply type `emulationstation` and press _Enter_)


### BBS connection
To ensure you can connect to the BBS to get a list of games later on, you will need will to install/update _wget_:

`sudo apt-get install wget`

### Configure Emulationstation

To create a new PICO-8 theme directory for Emulationstaion it's advised to follow this [step by step guide by dddaaannn](https://www.lexaloffle.com/bbs/?tid=3935). Just scroll down to the section _Launching PICO-8 from Emulation Station_ and follow the instructions.

Note: As the GBZ has a larger screen then the one mentioned in dddaaannns guide it's recommended to fit the resolution for the GBZ. Therefore make sure to edit the system config file like so:

    <system>
    <name>pico8</name>
    <fullname>PICO-8</fullname>
    <path>/home/pi/pico-8</path>
    <extension>.sh .SH .p8 .P8 .png .PNG</extension>
    <command>/opt/retropie/supplementary/runcommand/runcommand.sh 0 "/home/pi/pico-8/pico8 -height 256 -width 256 -pixel_perfect 0 -splore"</command>
    <platform>pico8</platform>
    <theme>pico8</theme>
    </system>

Note: At the moment the _-splore_ switch is set in lieu of the _-run_ switch. This is because PICO-8 doesn't allow yet to quit out of a game when using the -run switch in a shell script without having a keyboard plugged in. This might change in future updates. For the moment one has to run PICO-8 in splore mode. There you can exit the emulator via the GBZ controls.

***

### Configuring sound to run at normal speed
NOTE this is untested so far: 
* https://sudomod.com/forum/viewtopic.php?f=51&t=5425&p=57771#p57767
* https://www.lexaloffle.com/bbs/?tid=3935

### References: 
* https://www.lexaloffle.com/bbs/?tid=3935
* https://sudomod.com/forum/viewtopic.php?f=17&t=5020&p=53728
* https://sudomod.com/forum/viewtopic.php?t=5425