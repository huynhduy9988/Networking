Inter-VLan Routing using a Router
- Config a subinterface for VLAN 10
```sh
R1(config)# interface e0/0.1
R1(config-subif)# encapsulation dot1q 10
R1(config-subif)# ip add 192.168.1.1 255.255.255.0
```
- Config a subinterface for VLAN 20
```sh
R1(config)# interface e0/0.2
R1(config-subif)# encapsulation dot1q 20
R1(config-subif)# ip add 192.168.1.2 255.255.255.0
```
- Switch Trunk Configure
```sh
SW1(config)# interface e0/0
SW1(config-if)# switch-port trunk encapsulation dot1q
SW1(config-if)# switch-port mode trunk
SW1(config-if)# switch-port trunk allow vlan vlan-id
```
- EtherChannel on Switch Layer 3
```sh
DSW1(config)# interface range e0/0-1
DSW1(config-if)# no switch port
DSW1(config-if)# channel-group 1 mode on
DSW1(config-if)# exit
DSW1(config)# interface port-channel 1
DSW1(config-if)# no switch port
DSW1(config-if)# ip add 192.168.1.1 255.255.255.0
```
- EtherChannel on Switch Layer 2
```sh
DSW2(config)# interface range e0/0-1
DSW2(config-if)# channel-group 1 mode on
DSW2(config-if)# exit
DSW2(config)# interface port-channel 1
DSW2(config-if)# switch port trunk encapsulation dot1q
DSW2(config-if)# switch port mode trunk
```
