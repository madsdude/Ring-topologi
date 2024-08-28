```
Current configuration : 3445 bytes
!
! Last configuration change at 13:22:09 UTC Tue Aug 27 2024
!
version 15.2
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
service compress-config
!
hostname SW-LAN-14
!
boot-start-marker
boot-end-marker
!
!
!
no aaa new-model
!
!
ip cef
no ipv6 cef
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
!
interface Port-channel1
 switchport trunk encapsulation dot1q
 switchport mode trunk
!
interface Port-channel3
 switchport trunk encapsulation dot1q
 switchport mode trunk
!
interface GigabitEthernet0/0
 switchport trunk encapsulation dot1q
 switchport mode trunk
 negotiation auto
 channel-group 1 mode active
!
interface GigabitEthernet0/1
 switchport trunk encapsulation dot1q
 switchport mode trunk
 negotiation auto
 channel-group 1 mode active
!
interface GigabitEthernet0/2
 negotiation auto
!
interface GigabitEthernet0/3
 negotiation auto
!
interface GigabitEthernet1/0
 switchport trunk encapsulation dot1q
 switchport mode trunk
 negotiation auto
 channel-group 3 mode active
!
interface GigabitEthernet1/1
 switchport trunk encapsulation dot1q
 switchport mode trunk
 negotiation auto
 channel-group 3 mode active
!
interface GigabitEthernet1/2
 negotiation auto
!
interface GigabitEthernet1/3
 negotiation auto
!         
interface Vlan1
 ip address 192.168.1.17 255.255.255.0
!
ip forward-protocol nd
!
ip http server
ip http secure-server
!
ip route 0.0.0.0 0.0.0.0 192.168.1.1
ip ssh server algorithm encryption aes128-ctr aes192-ctr aes256-ctr
ip ssh client algorithm encryption aes128-ctr aes192-ctr aes256-ctr
!
!
control-plane
!
!
line con 0
line aux 0
line vty 0 4
!
!
end

```


