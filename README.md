# firmware_store

Release-Path: 

## Firmwarebau: bauen -> selbst testen -> beta -> stable
gluon$ make GLUON_BRANCH=stable
gluon$ make manifest GLUON_BRANCH=stable

## Signierung der Firmware:
Es gilt die Regel: man darf die Firmware erst signieren, nachdem man diese (aus dem factory-Ordner) selber auf stabilität und funktionlität getestet hat.
gluon$ contrib/sign.sh /PathToEcdsautilsSecret/secret images/sysupgrade/stable.manifest