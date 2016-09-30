# BLINUX-BLISUX-RootHack
Root hack for BLINUX/BLISUX (Epitech crappy version of OpenSUSE), working under HP EliteBook 840 G3 (School year 2016-2017)

As you know the new installed computers with BLISUX are displaying a custom boot menu that doesn't look like GNU Grub 2.

To change the root password to something you can use directly inside BLISUX terminal you'll have to get a root bash. To do that you have to change the BLISUX command line, you might say that's not possible as no options are specified in boot menu...

Indeed there is no option specified. Epitech succeeded to hide GNU Grub 2 and change the GUI interface to disturb the end user, but if you know the E key to edit the command, you can still enter the command line editor in order to edit the BLISUX 4.0 (El Tigre) startup command.
Now it's a bit more complicated as it uses EFI linux instead of legacy mode. Serach for the line that starts with linuxefi and go to the end of that line and type [SPACE] then type "init=/bin/bash". When you're done just type F10 on your keyboard to boot that new command line, wait while linux is loading, then you should be prompted with a full screen black terminal. Notice the "#" character after computer name, it means you are now identified as root.

You might want to type directly the passwd to change the root password, but that's not yet done, it can't be that easy, anyways if you got that far, don't worry not many steps are remaining. The operation is almost done.

So what you want to do first is remounting the file system as read/write instead of read-only. To proceed, type "mount -o remount,rw /". The command should end correctly.
Now you can finaly type "passwd" then type a new ROOT password, enter then type it again and do enter.

The root password is now changed. ROOT hack is now done. You can power off your machine.

Now you can boot normaly in BLISUX and enter your account password. If you still get the root command prompt, get back to the boot menu and type E again on the BLISUX (normaly first entry) and remove the "init=/bin/bash" parameter from the linux boot command. Then go back loading BLISUX.

To test if the hack worked, open a terminal in your BLISUX desktop environment. Then type su followed by [ENTER]. You get asked for the root password you just changed. Just enter the new updated ROOT password, then type enter again and BOOM enjoy full root access !!

HEHE !

Enjoy your new root access, you can do pretty much whatever you want now !

Message to BLISUX creators : It seam that despite all you could do to enforce the security or your distro, it's still not that good... Realy, think of allowing root access by default...

Yuri6037
