# beta- store

## Version 0.11.7 based on Gluon 2018.2.1

**Please only use this firmware-branch if you know how to fix things in case of trouble!**  

If every thing workes fine in this version it will be our base for some changes.  
This gluon-version 2018.2.1 has a gluon-scheduled-domain-switch which will be used for a breaking switch from IBSS to 802.11s.

My request to BETA-testers is: Please test this version and report any problems.

This releases has minor changes to 0.11.6 to manage the domain-switching.  

This software has a fixed change-set. It will break our old net on the scheduled date!!!!!  

I decided to switch to this new settings at  01. May 2019 04:00:00 MEZ  
New settings:  
1.) 802.11s instead of IBSS  
2.) 2.4HGz-channel 1 instead of channel 2  

This software is going to be rolled out for our new stable-release before scheduled switch-time unless any testing problems are reported SOON! **SO PLEASE HELP TESTING THIS FIRMWARE IF YOU CAN!**

You also can switch manually to the new settings any time you like via ssh and uci to test everything. 
The commands are:  

```
uci set gluon.core.domain="fftr_11s"  
gluon-reconfigure  
reboot  
```

and back to the old config:

```
uci set gluon.core.domain="fftr_ibss"  
gluon-reconfigure  
reboot  
```

To update your Router to this beta via autoupdater:  

```
autoupdater -f -b beta
```




See: [https://gluon.readthedocs.io/en/v2018.2.x/features/multidomain.html]


After frimware-upgrade to 0.11.7 your router should still be in our fftr_ibss -net!!  
If it comes up in the fftr_11s -net the firmware does not work as expected and **please report this to me**!!!  



yours
Tackin
