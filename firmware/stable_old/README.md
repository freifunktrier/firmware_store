# stable - store

## Version 0.11.11 based on Gluon 2018.2.4

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

