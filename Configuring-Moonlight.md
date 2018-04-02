# WORK IN PROGRESS
## Moonlight
1. Install this https://github.com/TechWizTime/moonlight-retropie
2. Edit file `/usr/share/moonlight/gamecontrollerdb.txt`
```
03000000412300003680000001010000,Arduino Leonardo,platform:Linux,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,a:b0,b:b1,x:b2,y:b3,start:b4,back:b5,leftshoulder:b6,rightshoulder:b8,lefttrigger:b7,righttrigger:b9,leftx:a0,lefty:a1,rightx:a2,righty:a3,
```
3.  moonlight stream -720 -fps 60 <IP> -input /dev/input/event0 -input /dev/input/event2

## Useful tools
- https://github.com/Grumbel/sdl-jstest