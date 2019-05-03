# Beta - store

## Version 0.11.8 based on Gluon 2018.2.1


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



See: [https://gluon.readthedocs.io/en/v2018.2.x/features/multidomain.html]


**Please only use this firmware-branch if you know how to fix things in case of trouble!**
