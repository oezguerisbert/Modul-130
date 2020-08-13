# RIP Basics:

## Aufgaben

### 1. PC IPs einrichten:

#### Die Konfigurationen:

```
    * PC0:
        - Gateway   :   192.168.1.1
        - Subnet    :   255.255.255.0
        - IP        :   192.168.1.10


    * PC1:
        - Gateway   :   192.168.2.1
        - Subnet    :   255.255.255.0
        - IP        :   192.168.2.10


    * PC2:
        - Gateway   :   192.168.3.1
        - Subnet    :   255.255.255.0
        - IP        :   192.168.3.10
```

#### Einstellungen:

    Einstellen per:
    1.  PC doppelklick
    2.  Tab: Desktop,
    3.  Oben links auf IP-Configuration
    4. Eingaben
        1. Gateway eingeben
        2. Subnetz eingeben
        3. IP eingeben
        4. Speichern

### 2. Einstellen der IP Adressen aller Interface der Router

1. #### Router0 öffnen:

```
    Router0> en
    Router0#> conf t
    Router0(config)# interface FastEthernet 0/0
    Router0(config-if)# ip address 192.168.4.1 255.255.255.0
    Router0(config-if)# no shutdown
    Router0(config-if)# exit
    Router0(config)# interface FastEthernet 0/1
    Router0(config-if)# ip address 192.168.1.1 255.255.255.0
    Router0(config-if)# no shutdown
    Router0(config-if)# exit
    Router0(config)# interface Ethernet 0/2/0
    Router0(config-if)# ip address 192.168.5.1 255.255.255.0
    Router0(config-if)# no shutdown
    Router0(config-if)# exit
    Router0(config)# exit
    Router0> write mem
```

2. #### Router1 öffnen:

```
    Router1> en
    Router1#> conf t
    Router1(config)# interface FastEthernet 0/0
    Router1(config-if)# ip address 192.168.6.1 255.255.255.0
    Router1(config-if)# no shutdown
    Router1(config-if)# exit
    Router1(config)# interface FastEthernet 0/1
    Router1(config-if)# ip address 192.168.3.1 255.255.255.0
    Router1(config-if)# no shutdown
    Router1(config-if)# exit
    Router1(config)# interface Ethernet 0/2/0
    Router1(config-if)# ip address 192.168.5.2 255.255.255.0
    Router1(config-if)# no shutdown
    Router1(config-if)# exit
    Router1(config)# exit
    Router1> write mem
```

3. #### Router2 öffnen:

```
    Router2> en
    Router2#> conf t
    Router2(config)# interface FastEthernet 0/0
    Router2(config-if)# ip address 192.168.4.2 255.255.255.0
    Router2(config-if)# no shutdown
    Router2(config-if)# exit
    Router2(config)# interface FastEthernet 0/1
    Router2(config-if)# ip address 192.168.6.2 255.255.255.0
    Router2(config-if)# no shutdown
    Router2(config-if)# exit
    Router2(config)# interface Ethernet 0/2/0
    Router2(config-if)# ip address 192.168.2.1 255.255.255.0
    Router2(config-if)# no shutdown
    Router2(config-if)# exit
    Router2(config)# exit
    Router2> write mem
```