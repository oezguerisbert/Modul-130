# Frequently Asked Questions


## __DynDNS:__

### Was ist ein DynDNS?
Ein DynDNS speichert eine IP-Adresse mit einer bestimmten Domain Name ab. Wenn er nicht weiß welche IP-Adresse zu dem Domain Name aufweist, fragt er einen weiteren DNS-Server.

### Wie funktioniert ein DynDNS?
* Bei Anfragen werden in einer Tabelle des DynDNS-Servers überprüft, ob eine IP-Adresse zu der Domain Name zugestellt wurde, und falls ein Eintrag vorhanden ist, wird diese IP zurückgeschickt. Ansonsten wird ein anderer DNS-Server angefragt.
* Jegliche Public IPs werden untereinander mit den anderen DynDNS-Servern synchronisert.
