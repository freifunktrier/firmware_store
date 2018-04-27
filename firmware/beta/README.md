# BETA - store

Please only use this firmware-branch if you know how to fix things in case of trouble!

DO NOT USE 0.10.5 ON .... 
Ubiquiti Airmax M2/M5 (NanoStation, Bullet, Loco, etc.) XM (XM board is the older, XW is the newer one.)  
XW Boards are not effected.
>lua -e 'print(require("platform_info").get_image_name())'  
answers you:  
ubiquiti-nanostation-loco-m2-xw   ->   You have an XW-Board  
ubiquiti-nanostation-loco-m2   ->   You have an XM-Board  

Gluon 2017.1.6 breaks the XM-Router in case you installed Gluon over a prior installed AirOS 5.6.15 firmware-version.
In this case the buggy AirOS 5.6.15-Bootloader is still active in gluon and makes trouble.  
I don't know how to find out if your Loco runs the AirOS 5.6.15-Bootloader or an earlier one.  

Please only use 0.10.5b - version (gluon 2017.7) for this devices!

https://github.com/freifunk-gluon/gluon/issues/1370