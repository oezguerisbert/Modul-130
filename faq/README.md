# Frequently Asked Questions

## __OPS:__

### Monitoring

#### SNMP
Für das Monitoring innerhalb einer Netwzwerkes wird das Prokotoll SNMP verwendet.
SNMP steht für **S**imple **N**etwork **M**onitoring **P**rotocol

beispiel-Software: ```nmap```


## __Ticket(system)__:

### Informationen:

- Eskalation 
    - Wer wird informiert nach wie viel Zeit vergangen ist und welche Massnahmen unternommen werden. 

- Reports 
    - Alle Komplikationen, Lösungen, Vorgang usw. werden Dokumentiert z.B. Wenn Kunde anruft und Mitarbeiter nicht verfügbar ist ein neuer Termin vereinbaren danach unbedingt Dokumentieren wann angerufen, wann ist der nächste Termin vereinbart wurde.
- Wissensdatenbank 
    - Common Solutions welche in 90% der Fälle eintreffen.

### Onsite bei Kunden
- Wenn es nicht mehr über Tel. lösbar ist, dann geht man zum Kunden und probiert das Problem Vorort zu lösen.
    - Material Liste, Verhalten, Piket (auf Abruf sein)
### Piket
-	Zeitlich definiert z.B. 
    - Montag 08:00 – Sonntag 07:59
    - Reaktionszeit: 15 Minuten
    - Vor Ort: 1 Stunde
-	Zeit gut planen, da man auf Abruf sein.
-	Werden entschädigt
-	Material + Transport
    - Materialliste
        - Ersatz Switch/ Router etc.
        - Laptop mit allem Adapter
        - LAN-Kabel
        - Werkzeug
        - Smartphone/ Ladekabel Powerbank/ Hotspot/ EU Datenvolumen
        - LAN-Kabel Tester/ Ersatz Kabel
        - Kontakt Kunde/ Kollege
        - Bilder Netzwerkpläne Doku/ Passwörter
        - Essen + Getränke
        - Geld/ Ausweis/ Benzin
-	Verhalten
    - Keine Ja/ nein Fragen (geschlossene Fragen)
    - Offene Fragen stellen

## __DynDNS:__

### Was ist ein DynDNS?
Ein DynDNS speichert eine IP-Adresse mit einer bestimmten Domain Name ab. Wenn er nicht weiß welche IP-Adresse zu dem Domain Name aufweist, fragt er einen weiteren DNS-Server.

### Wie funktioniert ein DynDNS?
* Bei Anfragen werden in einer Tabelle des DynDNS-Servers überprüft, ob eine IP-Adresse zu der Domain Name zugestellt wurde, und falls ein Eintrag vorhanden ist, wird diese IP zurückgeschickt. Ansonsten wird ein anderer DNS-Server angefragt.
* Jegliche Public IPs werden untereinander mit den anderen DynDNS-Servern synchronisert.
