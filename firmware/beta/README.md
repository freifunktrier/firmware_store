# BETA - store

Please only use this firmware-branch if you know how to fix things in case of trouble!

Updating an UBNT EdgeRouter X to Gluon v2018.1.2 reproducibly results in a brick.
The EdgeRouter X SFP seems to not be affected.
Further investigation is needed.


The previous gluon 2018.1 had a significant bug in the autoupdater.  
Please see also:  
[https://github.com/freifunk-gluon/gluon/issues/1496](https://github.com/freifunk-gluon/gluon/issues/1496)  
[https://forum.freifunk.net/t/gluon-2018-1-x-autoupdater-configverlust-gefahr/19322](https://forum.freifunk.net/t/gluon-2018-1-x-autoupdater-configverlust-gefahr/19322)  

The bug may lead to losing your node's config, ssh-key i.e. and boot into config-mode after update.  

So it is no good idea to use "autoupdater -f -b beta" via ssh to update from 0.11.1-beta to our new 0.11.3-beta.  
The more safer way is to use the sysupgrade-function.  

you may instead do:  

    cd /tmp  
    wget http://pegol.tackin.de/firmware/beta/sysupgrade/gluon-fftr-0.11.3+tackin.....sysupgrade.bin
 
or  

    cd /tmp  
    wget http://2.updates.services.fftr/firmware/beta/sysupgrade/gluon-fftr-0.11.3+tackin.....sysupgrade.bin  
(please add the right file for your node-type and node-version)

    echo 3 > /proc/sys/vm/drop_caches  
    sysupgrade gluon-fftr-0.11.3+tackin....sysupgrade.bin  


If you still want/need to take the risk, you may try an autoupdate.  I did my best to make it work and tested it on some routers with no problems.  
But as the older beta "gluon 0.11.1" also has a minor bug in the "beta.good.signatures", please make sure to first do  

    uci set autoupdater.beta.good_signatures='1'  
    autoupdater -f -b beta  


Tackin
