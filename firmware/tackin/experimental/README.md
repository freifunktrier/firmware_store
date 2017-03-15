# Tackin Experimental-Firmware

## Details:
Dieser Firmwarebuild basiert auf gluon 2016.2.4

Voreinstellung: autoupdate in "stable" Releases  
Wer also von dieser Experimental nicht auf dei nächste stable-release updaten möchte, muss im GUI das "autoupdate" deaktivieren.

Infos:  
Archer C7:  
Seltsame Dinge passieren, wenn man das Experimental-Sysupgrade einspielt und die im Router schon vorhandene Konfiguration übernimmt. Ihr müsst in dem Fall damit rechnen, dass der Router nicht mehr ins Freifunk-Netz findet, er keine Clients per LAN oder WLAN annimmt oder er den Client-Traffic einfach nicht weiterleitet.  Es ist also **keine gute Idee** diesen Router "aus der Ferne" mit einem Update zu versorgen! Nach einer sauberen Installation funktioniert mein Router aber perfekt ... na ja fast.  
Generell ist der Router mit dem neuen ath10k-Chip-Treiber ausgestattet. Die Unterstützung durch Gluon ist dabei derzeit leider nur rudimentär möglich. Meshing im 5GHz funktioniert nicht und ihr könnt neben dem WLAN-Clientnetz hier nur **11s** ODER **ibss** zum Meshen nutzen, aber nicht beides gleichzeitig. Mein Build nutzt ibss wie in unserem Netz derzeit üblich.

Ich kann mir vorstellen, dass dieses Verhalten auch bei anderen Routern auftreten kann. Bevor ihr also die Pferde scheu macht, bitte erst eine saubere Neuinstallation **ohne** Übernahme der vorhandenen Konfig durchführen und den Router anschließend ganz neu einrichten.  
Ihr würdet uns einen Gefallen tun, wenn ihr dabei vorher den **fastd-Key** der alten Konfig sichert und diesen nach dem Upgrade auch wieder einspielt. Dann müsst Ihr uns nicht einen neuen Key zumailen zum eintragen.  
SSH-Konsole:  
uci show fastd.mesh_vpn.secret  
Anzeige> fastd.mesh_vpn.secret='hier_steht_euer_secret_key'  

Neu einspielen:  
uci set fastd.mesh_vpn.secret='hier_steht_euer_secret_key'  
uci commit  
reboot  

