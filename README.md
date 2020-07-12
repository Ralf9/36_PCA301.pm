# 36_PCA301.pm

Funktioniert nun auch mit dem SIGNALDuino z.B. mit
https://wiki.fhem.de/wiki/Maple-SignalDuino

Es gibt für den SIGNALDuino nun 2 neue Attribute.

- ``"pollingStatus"``: wenn größer 0 dann wird alle x Sekunden ein "set statusRequest" gesendet, wenn ":0" angehängt wird (z.B. "600:0" polling alle 10 Min), dann wird bei "off" das polling statusRequest gestoppt.

- ``"sendMaxRetry" (default 4)``: damit kann angegeben werden, wie oft set on, off und statusRequest, wiederholt wird, falls es keine Antwort gibt.

Kanal ändern
====
Das Pollen des Statusrequest muß dafür gestoppt sein.
- in der DEF den Kanal ändern
- die Taste an der PCA301 solange drücken bis die LED blinkt, damit ist sie im Pairing Modus
- mit ``set pairing`` wird der neue Kanal an die PCA301 gesendet
