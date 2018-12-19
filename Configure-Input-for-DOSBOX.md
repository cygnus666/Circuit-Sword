## DOSBox mapper

To start a random app via [DOSBox](http://www.dosbox.com/wiki/Main_Page) you want to make sure to map all core keys to the equivalent CS controller buttons.
This can be done by launching the built in DOSBox mapper. For the following steps an USB Keyboard + Mouse is required.

To launch the mapper tool run the following commands in a terminal (press _F4_ on your keyboard to exit):

`cd /opt/retro*/em*/dosbox/bin`

`./dosbox -startmapper`

Alternatively you can press _CTRL+F1_ if you launched DOSBox from the main menu. 

![SAIO](https://s19.postimg.cc/rtz7g0o43/DOSBox.png)

Within this screen you now can remap the keyboard commands to the controller. (Make sure to visit the official [DOSBox wiki](http://www.dosbox.com/wiki/Mapper) on how to use this mapper.) When done, make sure to save and exit out of the mapper.

## Configure Joystick/apppad

However, when you start a random app via DOSBox, the D-pad/hat does no react to anything yet. So in the next step you also need to configure the DOSBox config file - `dosbox-SVN.conf` - which is located in the hidden folder `.dosbox` in your home folder. 
Again exit out via _F4_. Then type:

`cd ~/.dosbox`

`sudo nano dosbox-SVN.conf`

In the editor scroll down to the `[joystick]` section (+- line 193) until you find `joysticktype=auto` and change it to `joysticktype=fcs`. (For further reading: [DOSBox Manual](https://www.dosbox.com/DOSBoxManual.html#Joystick).)

Press _Ctrl+O_ to save your changes and _Ctrl+X_ to exit out of the nano editor. 

Now you can use all mapped buttons on your handheld device.


## Additional Notes

Depending on the app you intend to run, you might want to create different mapper files for each app since not all apps use the same key set. (else you can also search for app related patches, which allow a different kind of button usage.)

## See Also

* [How to configure USB app controllers in DOSBox.](http://dosonthepi.blogspot.co.uk/2015/01/configure-game-controllers-in-dosbox_29.html)
* [How to create a default mapping for controllers in DOSBox.](http://dosonthepi.blogspot.co.uk/2015/02/default-arcade-mapping-for-dosbox.html)
* [How to configure DOSBOX for individual apps.](http://dosonthepi.blogspot.co.uk/2015/02/dosbox-configuration-for-individual.html)