# I. EtherChannel
## 1. Topology
![](https://github.com/quangln94/Networking/blob/master/CCNP/SWITCH/Lab/Topology/EtherChannel.png)
## 2. Configure
-**Step 1**

***Config on DSW1***
```sh
DSW1>en
DSW1#conf t
DSW1(config)#int range e1/0-3
DSW1(config-if-range)#channel-group 1 mode active
DSW1(config-if-range)#exit
```
***Config on DSW2***
```sh
DSW2>en
DSW2#conf t
DSW2(config)#int range e1/0-3
DSW2(config-if-range)#channel-group 1 mode active
DSW2(config-if-range)#exit
```
-**Step 2**

***Config on DSW1***
```sh
DSW1>en
DSW1#conf t
DSW1(config)#int e0/0
DSW1(config-if-range)#channel-group 2 mode passive
DSW1(config)#int e0/3
DSW1(config-if-range)#channel-group 2 mode passive
```
***Config on SW1***
```sh
SW1>en
SW1#conf t
SW1(config)#int range e0/2-3
SW1(config-if-range)#channel-group 2 mode active
```
-**Step 3**

***Config on DSW2***
```sh
DSW2>en
DSW2#conf t
DSW2(config)#int e0/0
DSW2(config-if-range)#channel-group 2 mode passive
DSW2(config)#int e0/3
DSW2(config-if-range)#channel-group 2 mode passive
```
***Config on SW2***
```sh
SW2>en
SW2#conf t
SW2(config)#int range e0/2-3
SW2(config-if-range)#channel-group 2 mode active
```
