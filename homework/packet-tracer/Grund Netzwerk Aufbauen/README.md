# DCHP:

## Aufgaben

### Die Konfigurationen:

#### 1. DHCP:

1. Server öffnen
2. IP-Adresse des Servers festlegen:
    1. Tab > Config
    2. FastEthernet0
    3. IP Configuration > Static > ```192.168.1.10```
3. Tab > Services
4. serverPool auswählen
5. Die Einstellungen übernehmen:
```
Default Gateway     :   192.168.1.1
DNS Server          :   8.8.8.8
Start-IP Adresse    :   192.168.1.11
Subnetz Mask        :   255.255.255.0
Max. Number Users   :   245
```
6. PC's aus dem Netz 192.168.1.0 > DHCP aktivieren.
