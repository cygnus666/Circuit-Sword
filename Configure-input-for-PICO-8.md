## Map buttons for PICO-8

To start a random game via [PICO-8] Fantasy Console (https://www.lexaloffle.com/pico-8.php?page=faq) you want to make sure to map all core keys to the equivalent SAIO game controller buttons.

This can be done by editing the sdl_controllers.txt file in /home/pi/.lexaloffle folder:  
`nano /home/pi/.lexaloffle/pico-8/sdl_controllers.txt`

Once in the editor paste the following line:  
`03000000412300003680000001010000,Arduino LLC Arduino Leonardo,platform:Linux,x:b2,a:b1,b:b0,y:b3,back:b5,start:b4,dpleft:h0.8,dpdown:h0.4,dpright:h0.2,dpup:h0.1`

Save with:  
`Controll + X, then Y, then Enter`