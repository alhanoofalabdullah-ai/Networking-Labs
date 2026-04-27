# Project 18 - InterVLAN Routing (Router-on-a-Stick)

## Overview
This project demonstrates InterVLAN Routing using Router-on-a-Stick in Cisco Packet Tracer.

The network includes:

- Multiple VLANs
- Layer 2 Switch
- Router with Sub-Interfaces
- Static IP Configuration
- Trunk Port Configuration
- Server VLAN
- End-to-End Connectivity Testing using Ping

This project simulates a small enterprise network with separated departments and centralized server access.

---

## VLAN Structure

| VLAN ID | Name       | Department |
|---|---|---|
| 10 | HR | Human Resources |
| 20 | FINANCE | Finance |
| 30 | IT | IT Department |
| 40 | MANAGEMENT | Management |
| 50 | SERVERS | Server Network |

---

## Devices Used

- Cisco 2960 Switch
- Cisco 2911 Router
- Cisco 1941 Router
- 4 PCs
- 1 Server

---

## IP Addressing

### PCs

| Device | IP Address | Gateway |
|---|---|---|
| PC0 | 192.168.10.10 | 192.168.10.1 |
| PC1 | 192.168.20.10 | 192.168.20.1 |
| PC2 | 192.168.30.10 | 192.168.30.1 |
| PC3 | 192.168.40.10 | 192.168.40.1 |

### Server

| Device | IP Address | Gateway |
|---|---|---|
| Server0 | 192.168.50.10 | 192.168.50.1 |

---

## Features Implemented

- VLAN Creation
- Access Port Assignment
- Trunk Port Configuration
- Sub-Interface Configuration
- Dot1Q Encapsulation
- Static Routing
- InterVLAN Communication
- Server Reachability Testing

---

## Verification

Successful tests:

- PC to PC communication across VLANs
- PC to Server communication
- Router to Server communication
- Successful Ping verification

---

## Result

Project completed successfully with full InterVLAN communication and working Server VLAN access.

---

## Author

Alhanoof Alabdullah

GitHub Portfolio Project for Networking + Cybersecurity Career Development
