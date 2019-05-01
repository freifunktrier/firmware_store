# Beta - store

## Version 0.11.8 based on Gluon 2018.2.1

**Please only use this firmware-branch if you know how to fix things in case of trouble!**  


This firmware has no IBSS-mesh-support anymore, so it will **not** mesh with our net before 1. may 2019.
After our net has switched to 11s-mesh on 1. may 2019 you can fully use this version.
It will also be next stable to get finally rid of IBSS.  

This firmware has still multi-domain-support. It has an additional domain-set "fftr_11s_c11" to test an alternative environement on channel 11 instead of channel 1.
You can switch manually to the alternative settings any time you like via ssh and uci to test meshing on channel 11.  
The commands are:  

```
uci set gluon.core.domain="fftr_11s_c11"  
gluon-reconfigure  
reboot  
```

and back to the old config:

```
uci set gluon.core.domain="fftr_11s"  
gluon-reconfigure  
reboot  
```

To make the new alpha available for your router via autoupdater:  

```
uci add_list autoupdater.beta.mirror='http://2.updates.services.fftr/firmware/alpha/sysupgrade'
uci del_list autoupdater.beta.mirror='http://2.updates.services.fftr/firmware/beta/sysupgrade'
uci del_list autoupdater.beta.mirror='http://1.updates.services.fftr/firmware/beta/sysupgrade'
autoupdater -f -b beta
```

This makes this "alpha"-path to your routers "beta"-path.


See: [https://gluon.readthedocs.io/en/v2018.2.x/features/multidomain.html]


After frimware-upgrade to 0.11.7 your router should still be in our fftr_ibss -net!!  
If it comes up in the fftr_11s -net the firmware does not work as expected and **please report this to me**!!!  

