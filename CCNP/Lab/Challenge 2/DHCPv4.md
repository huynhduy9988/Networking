# 1
## 1. Topology
![](https://github.com/quangln94/CCNA/blob/master/CCNP/Lab/Challenge%202/Topology/ajax_helper.php.png)
## 2. Config
```sh
Core1>en
Core1#
Core1#conf t
Core1(config)#ip dhcp pool SALES
Core1(dhcp-config)#network 192.168.22.0 255.255.255.0
Core1(dhcp-config)#default-router 192.168.22.1
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4
Core1(dhcp-config)#exit
Core1(config)#ip dhcp excluded-address 192.168.22.1 192.168.22.10
Core1(config)#ip dhcp pool IT
Core1(dhcp-config)#network 192.168.33.0 255.255.255.0
Core1(dhcp-config)#default-router 192.168.2.1
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4
Core1(dhcp-config)#exit
Core1(config)#ip dhcp excluded-address 192.168.33.1 192.168.33.10
Core1(config)#
```
