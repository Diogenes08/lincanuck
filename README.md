This is the instruction file for a custom dCore Linux based project, which includes an i3 desktop, wifi, the Falkon Web Browser, Leafpad, and PCManFM file manager, as well as several scripts to make updating and adding software easier.
It boots 64bit by default for better hardware support, but can also be booted from a 32 bit kernel, with all applications and changes duplicated.

#####BASIC INSTRUCTIONS#####
You can use the mouse, but to start programs, you need to use keyboard shortcuts as described below in KEYBOARD
CONTROLS, or use dmenu(windows key + d button) as described below in COMMANDS.

Save any files you want to keep in /home/tc/files/.

Wifi/Ethernet/Phone Tethering and Volume are at the bottom right corner.

For Wifi, click the network icon at the bottom right corner, click refresh, click on Properties for your
network, select the encryption for your network, (usually WPA1/2 passphrase,) and enter your password,
and click OK. You should now be able to connect to the network.

For Ethernet or phone tethering, click Preferences and change wired interface to eth0 for ethernet, or
usb0 to use your phone's wifi through USB. Be sure to turn on tethering on your phone.

#####KEYBOARD CONTROLS#####
winkey is your windows key on your keyboard.

winkey + b              opens your web browser
winkey + m              opens a task manager
winkey + c              opens a file manager
winkey + t              opens a text editor

winkey + arrows         to switch windows
winkey + shift + arrows to move windows
winkey + shift + q      to close a window

winkey + w              to maximize a window/make tabbed windows
winkey + e              to tile windows next to each other. Press again to toggle horizontal and vertical
winkey + f              turn fullscreen off and on

winkey + 1-9            moves to that number desktop. Desktops with windows on them are listed bottom left.
                        The current desktop is shown in blue.
winkey + shift + 1-9    moves the current window to that desktop. The current window has a bright red title.

#####COMMANDS#####
winkey + d              opens a menu at the top where you can type commands like:

        README          open this README file
        browser         open the Falkon Web Browser
        texteditor      open the Leafpad Text Editor
        files           open the PCManFM File Manager
        wallpaper       change the wallpaper to a picture saved in /opt/backgrounds/
        sudo poweroff   to turn off your computer
        sudo reboot     to restart your computer

winkey + enter          opens a terminal where you can do the above commands, and the following:

        applist.sh      lists currently installed applications for ONBOOT(startup) and ONDEMAND(loaded when
                        used,) as well as files which are restored from backups made as described below
        update.sh       to update applications and install new applications listed in /home/tc/startup.lst
                        and /home/tc/app.lst
        clean.sh        clean up update files. The next update will have to download all packages again
        backup          backup changes to files and directories listed in /home/tc/backup.lst
