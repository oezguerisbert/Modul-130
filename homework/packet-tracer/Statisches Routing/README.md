# RIP Basics:

## Aufgaben

### 1. PC IPs einrichten:

#### Die Konfigurationen:

```
* PC1:
    - Gateway   :   192.168.1.1
    - Subnet    :   255.255.255.0
    - IP        :   192.168.1.10


* PC2:
    - Gateway   :   192.168.2.1
    - Subnet    :   255.255.255.0
    - IP        :   192.168.2.10


* PC3:
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

1. #### Router1 (CLI) öffnen:

```
Router1> en
Router1#> conf t
Router1(config)# interface FastEthernet 0/0
Router1(config-if)# ip address 10.0.0.2 255.0.0.0
Router1(config-if)# no shutdown
Router1(config-if)# exit
Router1(config)# interface FastEthernet 0/1
Router1(config-if)# ip address 12.0.0.1 255.0.0.0
Router1(config-if)# no shutdown
Router1(config-if)# exit
Router1(config)# interface Ethernet 0/2/0
Router1(config-if)# ip address 192.168.1.1 255.255.255.0
Router1(config-if)# no shutdown
Router1(config-if)# exit
Router1(config)#exit
Router1>write mem
```

2. #### Router2 (CLI) öffnen:

```
Router2> en
Router2#> conf t
Router2(config)# interface FastEthernet 0/0
Router2(config-if)# ip address 12.0.0.2 255.0.0.0
Router2(config-if)# no shutdown
Router2(config-if)# exit
Router2(config)# interface FastEthernet 0/1
Router2(config-if)# ip address 11.0.0.2 255.0.0.0
Router2(config-if)# no shutdown
Router2(config-if)# exit
Router2(config)# interface Ethernet 0/2/0
Router2(config-if)# ip address 192.168.2.1 255.255.255.0
Router2(config-if)# no shutdown
Router2(config-if)# exit
Router2(config)#exit
Router2>write mem
```

3. #### Router3 (CLI) öffnen:

```
Router3> en
Router3#> conf t
Router3(config)# interface FastEthernet 0/0
Router3(config-if)# ip address 10.0.0.1 255.0.0.0
Router3(config-if)# no shutdown
Router3(config-if)# exit
Router3(config)# interface FastEthernet 0/1
Router3(config-if)# ip address 11.0.0.1 255.0.0.0
Router3(config-if)# no shutdown
Router3(config-if)# exit
Router3(config)# interface Ethernet 0/2/0
Router3(config-if)# ip address 192.168.3.1 255.255.255.0
Router3(config-if)# no shutdown
Router3(config-if)# exit
Router3(config)#exit
Router3>write mem
```


### 3. Einstellen Manuelles Routing

1.  #### Router1 (CLI) öffnen:
    ```
    Router1>en
    Router1#conf t
    Router1(config)# ip route 192.168.2.0 255.255.255.0 12.0.0.2
    Router1(config)# ip route 192.168.3.0 255.255.255.0 10.0.0.1
    Router1(config)# ip route 11.0.0.1 255.255.255.0 10.0.0.1
    Router1(config)# ip route 11.0.0.2 255.255.255.0 10.0.0.1
    Router1(config)# exit
    Router1> exit
    Router1> write mem
    ```

2.  #### Router2 (CLI) öffnen:
    ```
    Router2> en
    Router2# conf t
    Router2(config)# ip route 192.168.1.0 255.255.255.0 12.0.0.1
    Router2(config)# ip route 192.168.3.0 255.255.255.0 11.0.0.1
    Router2(config)# ip route 10.0.0.1 255.255.255.0 11.0.0.1
    Router2(config)# ip route 10.0.0.2 255.255.255.0 11.0.0.1
    Router2(config)# exit
    Router2> exit
    Router2> write mem
    ```

2.  #### Router3 (CLI) öffnen:
    ```
    Router3> en
    Router3# conf t
    Router3(config)# ip route 192.168.1.0 255.255.255.0 10.0.0.2
    Router3(config)# ip route 192.168.2.0 255.255.255.0 11.0.0.2
    Router3(config)# ip route 10.0.0.1 255.255.255.0 11.0.0.2
    Router3(config)# ip route 10.0.0.2 255.255.255.0 11.0.0.2
    Router3(config)# exit
    Router3> exit
    Router3> write mem
    ```