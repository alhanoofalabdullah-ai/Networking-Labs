# README.md

# Project 17 — OSPF + EIGRP Route Redistribution | Cisco Packet Tracer

## Overview

This project demonstrates advanced dynamic routing using both OSPF and EIGRP with Route Redistribution between routing domains inside Cisco Packet Tracer.

The topology includes multiple routers, PCs, a server, and a Layer 2 switch, where:

- Router0 operates with OSPF
- Router1 operates with EIGRP
- Router2 acts as the redistribution router between OSPF and EIGRP

This project simulates enterprise-grade hybrid routing environments where multiple routing protocols must coexist and exchange routing information.

---

## Objectives

- Configure OSPF routing
- Configure EIGRP routing
- Implement route redistribution between OSPF and EIGRP
- Verify neighbor adjacency
- Validate routing table propagation
- Ensure full end-to-end connectivity

---

## Network Topology

Devices Used:

- 3 Routers
- 1 Switch
- 4 PCs
- 1 Server

Routing Design:

- OSPF Domain → Router0 ↔ Router2
- EIGRP Domain → Router1 ↔ Router2
- Redistribution Point → Router2

---

## IP Addressing Plan

### OSPF Link

| Device | Interface | IP Address |
|---|---|---|
| Router0 | G0/0/1 | 90.90.90.1/30 |
| Router2 | G0/1 | 90.90.90.2/30 |

### EIGRP Link

| Device | Interface | IP Address |
|---|---|---|
| Router1 | G0/0 | 100.100.100.1/30 |
| Router2 | G0/0 | 100.100.100.2/30 |

---

## Verification Commands

### OSPF

```bash
show ip ospf neighbor
show ip route

---

## EIGRP

show ip eigrp neighbors
show ip route

---

## Expected Results

## Successful outputs should show:

## OSPF Neighbor

FULL/DR

---

## EIGRP Neighbor

IP-EIGRP neighbors for process 100

---

## Route Redistribution

## Routes learned from both protocols should appear in:

show ip route

---

## with route codes:

O
D
D EX
O E2

---

## Skills Demonstrated

- Dynamic Routing
- OSPF Configuration
- EIGRP Configuration
- Route Redistribution
- Cisco CLI Troubleshooting
- Enterprise Network Design
- Packet Tracer Lab Implementation

---

Author

Prepared by:

Ahmed Alhanoof

Senior Digital Transformation & Enterprise Systems Specialist

Focused on:
PMIS | Enterprise Systems | Networking | Digital Governance | Infrastructure Technology
