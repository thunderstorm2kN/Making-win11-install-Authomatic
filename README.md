# Making-win11-install-Authomatic
In this repo branch I post the latest XML files I am using to install win11. The reasons are many why you need these, the main one is that these files reduce the installation times of win11 a lot by answering to the questions that the installer and OOBE ask you each time when installing the operating system. Made with schneegans.de generator

IN ORDER TO HAVE THE PROGRAM FUNCTIONING I AM REMINDING YOU THAT NAMING THE FILE autounattend.xml AND COPYING IT TO THE ROOT OF THE WINDOWS 11 INSTALLER STICK/MEDIA YOU MADE WITH RUFUS/VENTOY/Media creation tool is a must.
If the file is not in the correct place (where you open the win11 stick by double clicking on it) and is not named correctly (autounattend.xml) the win11 installer will ignore the file and ask you for all the questions. 

I am not forcefully debloating win11 with my programs I generated, as that could break some win11 features. 


The main reasons why I made these files: 
Got tired of clicking through OOBE and manually setting up accounts every time I installed Windows, so I put together an automated config using the Schneegans unattend generator. Tested it on a Ryzen 7 laptop over USB 2.0 — full install to a ready-to-use desktop in about 20 minutes (drivers still need to be added separately after).

What it actually does:

Skips the hardware checks (TPM, Secure Boot, RAM) so it'll install on machines that don't officially qualify for Win11
Sets up keyboard/language for three locales at once (I switch between English, Romanian and Norwegian layouts)
Skips the Microsoft account push — sets up a local account instead, no internet required during setup
Strips out the usual nags: Bing search integration, widgets, app suggestions, Edge's first-run popups, "consumer feature" ads baked into the Start menu
Applies those same settings to any new account you create later, not just the first one — so you're not redoing this per user
Cleans up after itself: deletes the leftover setup files (including anything that might have your WiFi password saved in plaintext) once first login is done

Everything runs automatically from a set of scripts bundled inside the single XML file — no extra USB partitions or separate files needed, it unpacks itself during setup.

Caveats:

Requires a valid Windows 11 license — this only automates setup, doesn't touch activation
The hardware bypass flags are meant for lab/testing, not something I'd push to a work fleet
No drivers included, that's still manual



Please make sure NOT to choose offline unless you actually plan installing win11 without wifi/Lan ethernet connection, this can reduce times as tested by us to 15/20 minutes of installation but will require you to plug in a usb cable or do android usb tethering because you will need installing drivers later. 

The online and offline versions are meant to install win11 pro with language support for Locales: English - Us, Romanian and Norwegian. 

Warning: Once you selected the ssd be careful as the installation will begin if you press next. 

After the installation the script makes the OOBE to ask you for network(where you press I dont have network for offline ver or connect to wifi/LAN if you use the other version), and to make a user name for the local user account and password(not compulsitory and you may click next if you dont need a password, advantage: you dont need a password to unlock/ start your win11 on your laptop anymore). 

after this windows will begin the updating process which is slow, I cannot fix MS servers unfortunately :)))) 

but nonetheless...  at some point the online ver will do 3 restarts (because win11 updates and installs new-ish drivers) and let you in the win11 desktop with its normal UI. 

Again, the offline ver will skip the updating process and make everything faster regarding writing win11 but you'll still have to wait a good amount of time for windows updates as they're needed to install drivers (and makes the process more automatic like this from my pov).  

If you made it until this point of the file, I want to thank you for using my software and to remind you that I do not assume responsibility for any damages or data loss. However I can promise that ALL that is posted here was tested at least once for installing win11 on one of my ASUS vivobook laptops (so both on AMD and INTEL platforms). If i found a bug I'd report it in the "File with bugs".  
