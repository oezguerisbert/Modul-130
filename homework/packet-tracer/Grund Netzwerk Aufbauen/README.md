# RIP Basics:

## Aufgaben

### 1. PC IPs einrichten:

#### Die Konfigurationen:

1. DHCP:
    1. Server öffnen
    2. IP-Adresse des Servers festlegen:
        1. Tab > Config
        2. FastEthernet0
        3. IP Configuration > Static
        4. Eingeben: ```192.168.1.10```
    3. Tab > Services
    4. serverPool auswählen
    5. Die Einstellungen übernehmen:
        1. Subnetz: ```255.255.255.0```
        2. IP-Range Anfang ```192.168.1.11```
        3. 