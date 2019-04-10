# 1
## 1. Topology
![](https://github.com/quangln94/CCNA/blob/master/CCNP/Lab/Challenge%202/Topology/ajax_helper.php.png)
## 2. Config
``sh
Core1>en
Core1#
Core1#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
*Apr 10 01:40:08.942: %LINK-3-UPDOWN: Interface Vlan22, changed state to up
*Apr 10 01:40:09.942: %LINEPROTO-5-UPDOWN: Line protocol on Interface Vlan22, changed state to up
Core1(config)#ip dhcp pool SALES
Core1(dhcp-config)#network 192.168.22.0 255.255.255.0
Core1(dhcp-config)#default-router 192.168.22.1
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4
Core1(dhcp-config)#ip dhc
Core1(dhcp-config)#ip dhcp po
Core1(dhcp-config)#
Core1(dhcp-config)#
Core1(dhcp-config)#exit
Core1(config)#
Core1(config)#ip dhcp
Core1(config)#ip dhcp po
Core1(config)#ip dhcp pool IT
Core1(dhcp-config)#netwo
Core1(dhcp-config)#network 192.168.33.0 255.255.255.0
Core1(dhcp-config)#dea
Core1(dhcp-config)#def
Core1(dhcp-config)#default-router 192.168.2.1
Core1(dhcp-config)#dns
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4
Core1(dhcp-config)#exit
Core1(config)#ip dhc
Core1(config)#ip dhcp e
Core1(config)#ip dhcp excluded-address 192
Core1(config)#ip dhcp excluded-address 192.168.22.1 192.168.22.10
Core1(config)#ip dhcp excluded-address 192.168.33.1 192.168.33.10
Core1(config)#
hcp excluded-address 192.168.33.1 192.168.33.10
```
