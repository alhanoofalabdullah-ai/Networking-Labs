# Project 10 — Dynamic DHCP + VLAN + NAT Overload (Enterprise Level)

## Overview
This project demonstrates an enterprise-style network in Cisco Packet Tracer that combines VLAN segmentation, trunking, router-on-a-stick inter-VLAN routing, DHCP services for multiple VLANs, and NAT overload for outbound connectivity simulation.

The lab is designed to show how a router can:
- Route traffic between multiple VLANs
- Provide DHCP scopes for different departments
- Translate multiple inside private IP addresses to a single outside public IP using NAT overload

## Objectives
- Build a segmented network using VLANs
- Configure access ports for end devices
- Configure a trunk link between the switch and router
- Enable router-on-a-stick using subinterfaces
- Configure DHCP pools for each VLAN
- Configure NAT overload for inside users
- Verify dynamic IP assignment and gateway reachability

## Topology
- **Switch0**
- **Router0**
- **PC0**
- **PC1**
- **PC2**
- **PC3**
- **PC4**
- **Server0**

## VLAN Design
| VLAN ID | Name  | Subnet            | Default Gateway |
|--------:|-------|-------------------|-----------------|
| 10      | SALES | 192.168.10.0/24   | 192.168.10.1    |
| 20      | HR    | 192.168.20.0/24   | 192.168.20.1    |

## IP Plan
### Router Subinterfaces
- `G0/0/0.10` → `192.168.10.1/24`
- `G0/0/0.20` → `192.168.20.1/24`

### Outside Interface
- `G0/0/1` → `200.1.1.1/24`

### Server
- Static IP used for internal service hosting

## Key Features
- VLAN segmentation for department isolation
- Trunk communication between switch and router
- Inter-VLAN routing using router subinterfaces
- DHCP per VLAN
- NAT overload for multi-host outbound translation
- Enterprise-style logical design

## Switch Configuration Summary
- VLAN 10 created as **SALES**
- VLAN 20 created as **HR**
- Access ports assigned to end devices
- Trunk port configured toward the router

## Router Configuration Summary
- Router-on-a-stick enabled using IEEE 802.1Q encapsulation
- DHCP pools created for VLAN 10 and VLAN 20
- Excluded gateway and reserved addresses from DHCP assignment
- NAT inside configured on VLAN subinterfaces
- NAT outside configured on external interface
- ACL used to define inside local networks for overload translation

## Verification
The following checks were performed:
- VLANs appeared correctly in `show vlan brief`
- Trunk status verified using `show interfaces trunk`
- Router subinterfaces verified using `show ip interface brief`
- DHCP clients successfully received IP addresses dynamically
- End devices successfully pinged their VLAN gateways
- NAT translations verified with:
  - `show ip nat translations`

## Expected Results
- VLAN 10 clients receive addresses from `192.168.10.0/24`
- VLAN 20 clients receive addresses from `192.168.20.0/24`
- Each client can ping its correct default gateway
- Multiple inside hosts can be translated through one outside interface using NAT overload

## Skills Practiced
- VLAN implementation
- Access and trunk port assignment
- Router-on-a-stick
- DHCP configuration
- NAT overload
- IP subnet planning
- Verification and troubleshooting

## Files Included
- `project10.pkt`
- `config.txt`
- `README.md`

## Author
**Alhanoof Alabdullah**  
Networking Labs Portfolio
