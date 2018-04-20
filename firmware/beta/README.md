# BETA - store

Please only use this firmware-branch if you know how to fix things in case of trouble!

DO NOT USE ON ....  
Ubiquiti NanoStation Loco M2 XM (XM board is the older, XW is the newer one.)  
>lua -e 'print(require("platform_info").get_image_name())'  
answers you:  
ubiquiti-nanostation-loco-m2-xw   ->   You have an XW-Board  
ubiquiti-nanostation-loco-m2   ->   You have an XM-Board  

Gluon 2017.1.6 breaks the XM-Router in case you installed Gluon over a prior installed AirOS 5.6.15 firmware-version.
At the moment I can only warn to update!  

https://github.com/freifunk-gluon/gluon/issues/1370