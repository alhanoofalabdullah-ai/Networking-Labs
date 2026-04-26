# Project 15 — OSPF Multi Router Dynamic Routing

## Overview

This project demonstrates OSPF (Open Shortest Path First) dynamic routing configuration using multiple Cisco routers in Cisco Packet Tracer.

The lab focuses on establishing OSPF neighbor adjacency, route advertisement, routing table verification, and end-to-end connectivity between multiple network segments.

This project is designed as part of advanced enterprise networking practice for real-world routing environments.

---

## Objectives

- Configure OSPF dynamic routing
- Establish OSPF neighbor relationships
- Verify FULL adjacency state
- Validate routing table propagation
- Test end-to-end network communication
- Simulate enterprise multi-router routing design

---

## Topology

Devices Used:

- 3 Routers
- 1 Switch
- 4 PCs
- 1 Server

Routing Design:

- Router0 ↔ Router2 → OSPF
- Router1 ↔ Router2 → OSPF
- Internal VLAN networks connected through Router0

---

## IP Addressing Plan

### Router0

| Interface | IP Address |
|---|---|
| G0/0/1 | 70.70.70.1 /30 |

---

### Router1

| Interface | IP Address |
|---|---|
| G0/1 | 80.80.80.1 /30 |

---

### Router2

| Interface | IP Address |
|---|---|
| G0/0 | 80.80.80.2 /30 |
| G0/1 | 70.70.70.2 /30 |

---

## OSPF Configuration

### OSPF Process ID

```bash
router ospf 1

---

## Area Used

Area 0

---

## Verification Commands

## Check OSPF Neighbors

show ip ospf neighbor

---

## Expected Result:

FULL/DR

---

## Check Routing Table

show ip route

---

## Expected Result:

O = OSPF Learned Routes

---

## Final Result

## Successfully achieved:

- FULL OSPF Neighbor Adjacency
- Dynamic Route Exchange
- Routing Table Population
- Stable Multi-Router Communication

---

## Project Status:

- SUCCESSFULLY COMPLETED
- Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
- Dynamic Routing Protocols
- OSPF Area 0 Design

---

Author

Prepared by:

Alhanoof Alabdullah

Senior Digital Transformation & Enterprise Systems Specialist
