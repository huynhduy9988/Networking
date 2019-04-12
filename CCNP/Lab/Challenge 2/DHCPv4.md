# 1
## 1. Topology
![](https://github.com/quangln94/CCNA/blob/master/CCNP/Lab/Challenge%202/Topology/ajax_helper.php.png)
## 2. Config
- **Step 1**

***Config on Core1***
```sh
Core1>en
Core1#
Core1#conf t
Core1(config)#int vlan 22
Core1(config-if)#ip add 192.168.22.1 255.255.255.0
Core1(config-if)#exit
Core1(config)#ip dhcp pool SALES
Core1(dhcp-config)#network 192.168.22.0 255.255.255.0
Core1(dhcp-config)#default-router 192.168.22.2
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4 
Core1(dhcp-config)#exit
Core1#clear ip dhcp binding *   # Command clear IP daa cap trong POOL
```
***Config on PC1, PC2***
```sh
PC1>en
PC1#conf t
PC1(config)#int e0/0
PC1(config-if)#ip address dhcp
```
- **Step 2**

***Config on Core1***
```sh
Core1>en
Core1#
Core1#conf t
Core1(config)#int e0/2
Core1(config-if)#ip add 192.168.2.1 255.255.255.0
Core1(config-if)#exit
Core1(config)#ip dhcp pool IT
Core1(dhcp-config)#network 192.168.33.0 255.255.255.0
Core1(dhcp-config)#default-router 192.168.33.2
Core1(dhcp-config)#dns-server 8.8.8.8 8.8.4.4
Core1(dhcp-config)#exit
Core1(config)#ip dhcp excluded-address 192.168.33.1 192.168.33.10
Core1(config)#exit
```
- **Config on Switch 2**
```sh
SW2>en
SW2#conf t
SW2(config)#vlan 33
SW2(config-vlan)#int vlan 33
SW2(config-if)#ip add 192.168.33.1 255.255.255.0
SW2(config-if)#no sh
SW2(config-if)#ip helper-address 192.168.2.1
```
***Config on PC3, SRV***
```sh
PC3>en
PC3#conf t
PC3(config)#int e0/0
PC3(config-if)#ip address dhcp
```
