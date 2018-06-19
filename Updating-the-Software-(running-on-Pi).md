# Enable SSH
Enabling SSH allows you to log in to the Pi remotely (e.g. using PuTTY)

1. From retropie menu, go to 'settings' page
2. Open 'raspi-config' option
3. Press DOWN to 'interface options'
4. Press RIGHT (to select the 'OK' button) and then press 'B' to select
5. Press DOWN to 'SSH'
6. Press RIGHT (to select the 'OK' button) and then press 'B' to select
7. Press LEFT (to select the 'ENABLE' button) and then press 'B' to select
8. Press RIGHT twice (to get to 'EXIT/BACK' button) and then press 'B' to select

# Updating the Circuit Sword software
The installation includes an update script! This will perform the necessary actions to pull latest changes and apply them to your running installation.

1. Enable WIFI and SSH
2. SSH into Pi
3. `cd Circuit-Sword`
4. `sudo ./update.sh`