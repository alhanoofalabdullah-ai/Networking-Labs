# Project 16 — EIGRP Multi Router Dynamic Routing

## Overview

This project demonstrates EIGRP (Enhanced Interior Gateway Routing Protocol) dynamic routing configuration using multiple Cisco routers in Cisco Packet Tracer.

The lab focuses on establishing EIGRP neighbor adjacency, dynamic route exchange, routing table verification, and end-to-end connectivity across multiple network segments.

This project simulates real-world enterprise dynamic routing design using Cisco EIGRP protocol.

---

## Objectives

- Configure EIGRP dynamic routing
- Establish EIGRP neighbor relationships
- Verify successful neighbor adjacency
- Validate routing table propagation
- Test end-to-end communication
- Simulate enterprise multi-router routing environments

---

## Topology

Devices Used:

- 3 Routers
- 1 Switch
- 4 PCs
- 1 Server

Routing Design:

- Router0 ↔ Router2 → EIGRP
- Router1 ↔ Router2 → EIGRP
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

## EIGRP Configuration

### Autonomous System Number

```bash
router eigrp 100

---

## Recommended Command

no auto-summary

---

## Verification Commands
##Check EIGRP Neighbors

show ip eigrp neighbors

---

## Expected Result:

Neighbor adjacency established successfully

---

## Check Routing Table

show ip route

---

## Expected Result:

D = EIGRP Learned Routes

---

## Final Result

## Successfully achieved:

- EIGRP Neighbor Adjacency
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
- EIGRP Enterprise Routing Design

---

Author

Prepared by:

Alhanoof Alabdullah

Senior Digital Transformation & Enterprise Systems Specialist
