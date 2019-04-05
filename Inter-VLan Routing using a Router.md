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
