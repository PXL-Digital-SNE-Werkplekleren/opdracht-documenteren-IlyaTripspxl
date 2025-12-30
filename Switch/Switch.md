# Switch Configuratie

<details class="details-section">
	<summary class="section-summary">Switch Configuratie</summary>

```
Building configuration...

Current configuration : 2186 bytes
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname SW-DEV-01
!
enable secret 5 $1$mERr$5.a6P4JqbNiMX01usIfka/
!
!
!
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/2
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/3
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/4
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/5
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/6
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/7
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/8
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/9
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/10
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/11
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/12
switchport access vlan 10
switchport mode access
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
description Verbinding_naar_Router_G0/0/0
switchport access vlan 10
switchport mode trunk
!
interface GigabitEthernet0/2
!
interface Vlan1
no ip address
shutdown
!
interface Vlan10
ip address 192.168.0.2 255.255.255.224
!
ip default-gateway 192.168.0.1
!
banner motd ^C
==========================================
AUTHORIZED PERSONAL ONLY
========================================== ^C
!
!
!
line con 0
password 7 082243401A16091243595F
login
!
line vty 0 4
password 7 082243401A16091243595F
login
transport input ssh
line vty 5 15
password 7 082243401A16091243595F
login
!
!
!
!
end

```
</details>
