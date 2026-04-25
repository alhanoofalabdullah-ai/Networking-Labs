# Project 11 — Enterprise Secure Network

## Overview

This project demonstrates a secure enterprise-level network using Cisco Packet Tracer with NAT overload, inter-router routing, server management, and internal network segmentation.

The lab simulates a real-world business environment where secure outbound connectivity and protected internal resources are required.

---

## Network Topology

### Devices Used

- 1 Cisco 2960 Switch
- 2 Routers (PT8200 + Cisco 1941)
- 5 PCs
- 1 Server
- Internal Secure LAN
- Routed WAN Connection

---

## IP Addressing

### Internal Network

| Device | IP Address |
|---|---|
| Router0 LAN | 192.168.10.1 |
| PC0 | 192.168.10.10 |
| PC1 | 192.168.10.11 |
| PC2 | 192.168.10.12 |
| PC3 | 192.168.10.13 |
| PC4 | 192.168.10.14 |
| Server | 192.168.10.100 |

### WAN Connection

| Device | IP Address |
|---|---|
| Router0 WAN | 200.1.1.1 |
| Router1 WAN | 200.1.1.2 |

---

## Security Features

- NAT Overload (PAT)
- Static Routing
- Secure Internal Access
- Enterprise Segmentation
- Server Resource Protection
- Controlled Internet Access

---

## Verification

### Test Commands

```bash
show ip interface brief
show ip route
show access-lists
show ip nat translations
ping 200.1.1.2
ping 8.8.8.8

---------------------

## Learning Outcomes

## This project helps demonstrate:

- Enterprise Network Design
- Cisco Routing
- NAT Configuration
- Secure Network Architecture
- Real-world IT Infrastructure Skills

---------------------
Author

Alhanoof Alabdullah

Senior Digital Transformation & Enterprise Systems Specialist
