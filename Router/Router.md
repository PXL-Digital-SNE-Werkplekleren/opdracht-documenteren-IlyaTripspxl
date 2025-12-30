# Router Configuratie

<details class="details-section">
	<summary class="section-summary">Router Configuratie</summary>

```
Using 1599 bytes
!
version 15.4
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
security passwords min-length 8
!
hostname Router
!
!
!
enable secret 5 $1$mERr$5.a6P4JqbNiMX01usIfka/
!
!
!
!
!
!
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface GigabitEthernet0/0/0
 no ip address
 duplex auto
 speed auto
!
interface GigabitEthernet0/0/0.10
 encapsulation dot1Q 10
 ip address 192.168.0.1 255.255.255.224
 ipv6 address 2001:DB8:1::1/64
!
interface GigabitEthernet0/0/1
 no ip address
 duplex auto
 speed auto
!
interface GigabitEthernet0/0/1.20
 encapsulation dot1Q 20
 ip address 192.168.0.33 255.255.255.224
 ipv6 address 2001:DB8:2::1/64
!
interface GigabitEthernet0/0/1.30
 encapsulation dot1Q 30
 ip address 192.168.0.65 255.255.255.224
 ip access-group 101 in
 ipv6 address 2001:DB8:3::1/64
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
ip access-list extended GASTEN_BLOCK
 deny ip 192.168.0.48 0.0.0.15 192.168.0.0 0.0.0.31
 deny ip 192.168.0.48 0.0.0.15 192.168.0.32 0.0.0.15
 permit ip any any
access-list 101 deny ip 192.168.0.64 0.0.0.31 192.168.0.0 0.0.0.31
access-list 101 deny ip 192.168.0.64 0.0.0.31 192.168.0.32 0.0.0.31
access-list 101 permit ip any any
!
banner motd ^C
==========================================
AUTHORIZED PERSONAL ONLY
========================================== ^C
!
!
!
!
line con 0
 password 7 082243401A16091243595F
 login
!
line aux 0
!
line vty 0 4
 password 7 082243401A16091243595F
 login
!
!
!
end
```
</details>
