# Project 12 — Advanced VLAN + Inter-VLAN Routing + ACL Security

## Overview

This project demonstrates enterprise-grade VLAN segmentation with Inter-VLAN routing using Router-on-a-Stick and Access Control List (ACL) security restrictions.

The goal is to simulate a secure corporate network where departments are isolated logically while allowing controlled communication between them.

---

## Network Topology

### Devices Used

- 1 Cisco 2960 Switch
- 1 Router
- 5 PCs
- 1 Server

---

## VLAN Structure

| VLAN | Department |
|---|---|
| VLAN 10 | HR |
| VLAN 20 | Finance |
| VLAN 30 | IT |
| VLAN 40 | Server Zone |

---

## Security Policy

### ACL Rule

Finance Department (VLAN 20) is NOT allowed to access the Server Zone (VLAN 40).

All other traffic is allowed.

This simulates real-world access restriction policies for sensitive business systems.

---

## Features Implemented

- VLAN Segmentation
- Inter-VLAN Routing
- Router-on-a-Stick
- Trunk Port Configuration
- ACL Security Enforcement
- Department Isolation
- Server Protection

---

## Verification

### Test Commands

```bash
show vlan brief
show interfaces trunk
show ip interface brief
show access-lists
ping tests between VLANs

---------------

## Learning Outcomes

## This project demonstrates:

- Secure VLAN Design
- Enterprise Network Segmentation
- Router Sub-Interfaces
- ACL-Based Security
- Controlled Access Architecture

----------------------------------
Author

Alhanoof Alabdullah

Senior Digital Transformation & Enterprise Systems Specialist
