# Hybrid-Network-Simulationn
A comprehensive project designing &amp; simulating five core network topologies (Bus, Mesh, Star, Ring, Extended Star) and a complex hybrid network. Features dual-stack IPv4/IPv6, VLANs, security, servers (HTTP/DNS/DHCP), and an advanced EIGRP configuration. Fully documented on GitHub.
# Hybrid-Network-Simulation
A comprehensive project designing &amp; simulating five core network topologies (Bus, Mesh, Star, Ring, Extended Star) and a complex hybrid network. Features dual-stack IPv4/IPv6, VLANs, security, servers (HTTP/DNS/DHCP), and an advanced EIGRP configuration. Fully documented on GitHub.
Final-Assignments/
├─ Assignment1/
│   └─ FINAL_merliciaa1.pkt



| **Device**  | **IPv4 Address** | **IPv6 Address** | **VLAN1**    |
| ----------- | ---------------- | ---------------- | ------------ |
| PC0         | 192.168.1.1      | 2001:DB8:1::1    | —            |
| PC1         | 192.168.1.2      | 2001:DB8:1::2    | —            |
| PC2         | 192.168.1.3      | 2001:DB8:1::3    | —            |
| PC3         | 192.168.1.4      | 2001:DB8:1::4    | —            |
| PC4         | 192.168.1.5      | 2001:DB8:1::5    | —            |
| PC5         | 192.168.1.18     | 2001:DB8:1::18   | —            |
| PC6         | 192.168.1.19     | 2001:DB8:1::19   | —            |
| PC7         | 192.168.1.20     | 2001:DB8:1::20   | —            |
| PC8         | 192.168.1.6      | 2001:DB8:1::6    | —            |
| PC9         | 192.168.1.9      | 2001:DB8:1::9    | —            |
| PC10        | 192.168.1.8      | 2001:DB8:1::8    | —            |
| PC11        | 192.168.1.7      | 2001:DB8:1::7    | —            |
| PC12        | 192.168.1.10     | 2001:DB8:1::10   | —            |
| PC13        | 192.168.1.11     | 2001:DB8:1::11   | —            |
| PC14        | 192.168.1.12     | 2001:DB8:1::12   | —            |
| PC15        | 192.168.1.13     | 2001:DB8:1::13   | —            |
| PC16        | 192.168.1.14     | 2001:DB8:1::14   | —            |
| PC17        | 192.168.1.16     | 2001:DB8:1::16   | —            |
| PC18        | 192.168.1.17     | 2001:DB8:1::17   | —            |
| PC19        | 192.168.1.15     | 2001:DB8:1::15   | —            |
| StarSwitch1 | —                | —                | 192.168.1.36 |
| RingSwitch1 | —                | —                | 192.168.1.22 |
| RingSwitch2 | —                | —                | 192.168.1.23 |
| RingSwitch3 | —                | —                | 192.168.1.24 |
| RingSwitch4 | —                | —                | 192.168.1.35 |
| BusSwitch1  | —                | —                | 192.168.1.32 |
| BusSwitch2  | —                | —                | 192.168.1.33 |
| BusSwitch3  | —                | —                | 192.168.1.34 |
| MeshSwitch1 | —                | —                | 192.168.1.28 |
| MeshSwitch2 | —                | —                | 192.168.1.29 |
| MeshSwitch3 | —                | —                | 192.168.1.30 |
| MeshSwitch4 | —                | —                | 192.168.1.31 |
| Switch1     | —                | —                | 192.168.1.25 |
| Switch2     | —                | —                | 192.168.1.26 |
| Switch3     | —                | —                | 192.168.1.27 |
| Server1     | 192.168.1.37     | 2001:DB8:1::37   | —            |



⚙️ VLAN Configuration Notes

Standard Switch Configuration Template:

Switch> enable
Switch# configure terminal 
Switch(config)# hostname [Switch_Name]
[Switch_Name](config)# interface vlan1
[Switch_Name](config-if)# ip address [IP_Address] [Subnet_Mask]
[Switch_Name](config-if)# no shutdown 
[Switch_Name](config-if)# exit
[Switch_Name](config)# exit
[Switch_Name]#


Assigning Port to VLAN 1:

Switch> enable
Switch# configure terminal
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 1
Switch(config-if)# no shutdown
Switch(config-if)# exit

🔐 Basic Security Configuration
Switch> enable
Switch# configure terminal
Switch(config)# enable password Merl
Switch(config)# exit
Switch# copy running-config startup-config

🌐 Web Server Configuration

A custom index.html file was created to simulate a web server page titled AETHER FILE SERVER.
It includes HTML, CSS, and JavaScript to provide an interactive file system interface hosted on the HTTP server.


├─ Assignment2/
│   └─ [files for Assignment 2]
# Part II – EIGRP Network Configuration

## Overview
This network consists of 4 routers and 4 PCs configured using **EIGRP** for dynamic routing. 
The network includes multiple subnets, point-to-point links, 
and LAN connections for PCs. The configuration ensures proper routing between all devices.

---

## IP Address Table

| Device   | IPv4 Address        | Subnet Mask       | Default Gateway |
|----------|------------------|-----------------|----------------|
| Router0 G0/0 | 10.10.10.2/30  | 255.255.255.252 | --             |
| Router0 G0/1 | 10.10.10.9/30  | 255.255.255.252 | --             |
| Router1 G0/0 | 10.10.10.10/30 | 255.255.255.252 | --             |
| Router1 G0/1 | 10.10.10.14/30 | 255.255.255.252 | --             |
| Router1 G0/2 | 192.168.2.1/24 | 255.255.255.0   | --             |
| Router2 G0/0 | 10.10.10.6/30  | 255.255.255.252 | --             |
| Router2 G0/1 | 10.10.10.13/30 | 255.255.255.252 | --             |
| Router2 G0/2 | 192.168.2.1/24 | 255.255.255.0   | --             |
| Router3 G0/0 | 10.10.10.5/30  | 255.255.255.252 | --             |
| Router3 G0/1 | 10.10.10.1/30  | 255.255.255.252 | --             |
| Router3 G0/2 | 192.168.1.1/24 | 255.255.255.0   | --             |
| PC0          | 192.168.1.20   | 255.255.255.0   | 192.168.1.1   |
| PC1          | 192.168.1.10   | 255.255.255.0   | 192.168.1.1   |
| PC2          | 192.168.2.10   | 255.255.255.0   | 192.168.2.1   |
| PC3          | 192.168.2.20   | 255.255.255.0   | 192.168.2.1   |

---

## Router Configurations

### Router0 (R0)
```bash
enable
configure terminal
hostname R0
interface GigabitEthernet0/0
 ip address 10.10.10.2 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/1
 ip address 10.10.10.9 255.255.255.252
 no shutdown
exit

Router1 (R1)
enable
configure terminal
hostname R1
interface GigabitEthernet0/0
 ip address 10.10.10.10 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/1
 ip address 10.10.10.14 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/2
 ip address 192.168.2.1 255.255.255.0
 no shutdown
exit

router eigrp 100
 network 10.10.10.8 0.0.0.3
 network 10.10.10.12 0.0.0.3
 network 192.168.2.0 0.0.0.255
 no auto-summary
exit

Router2 (R2)
enable
configure terminal
hostname R2
interface GigabitEthernet0/0
 ip address 10.10.10.6 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/1
 ip address 10.10.10.13 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/2
 ip address 192.168.2.1 255.255.255.0
 no shutdown
exit

router eigrp 100
 network 10.10.10.4 0.0.0.3
 network 10.10.10.12 0.0.0.3
 network 192.168.2.0 0.0.0.255
 no auto-summary
exit

Router3 (R3)

enable
configure terminal
hostname R3
interface GigabitEthernet0/0
 ip address 10.10.10.5 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/1
 ip address 10.10.10.1 255.255.255.252
 no shutdown
exit
interface GigabitEthernet0/2
 ip address 192.168.1.1 255.255.255.0
 no shutdown
exit

router eigrp 100
 network 10.10.10.0 0.0.0.3
 network 10.10.10.4 0.0.0.3
 network 192.168.1.0 0.0.0.255
 no auto-summary
exit


