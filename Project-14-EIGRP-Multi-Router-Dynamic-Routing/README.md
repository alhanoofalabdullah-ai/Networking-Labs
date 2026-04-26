# Project-14-EIGRP-Multi-Router-Dynamic-Routing

## Cisco Packet Tracer Lab – EIGRP Dynamic Routing Between Three Routers

This project demonstrates the configuration of Enhanced Interior Gateway Routing Protocol (EIGRP) between three Cisco routers using Cisco Packet Tracer.

The lab focuses on establishing neighbor relationships, exchanging routing information dynamically, and validating connectivity across multiple network segments.

---

## Project Objectives

- Configure EIGRP on multiple routers
- Establish EIGRP neighbor adjacency
- Enable dynamic route exchange
- Verify learned routes using routing tables
- Test end-to-end connectivity using ping
- Simulate enterprise-level routing behavior

---

## Network Topology

### Devices Used

- 3 Routers
- 1 Switch
- 4 PCs
- 1 Server

### Routing Connections

- Router0 ↔ Router2 → Network: 60.60.60.0/30
- Router1 ↔ Router2 → Network: 50.50.50.0/30

### Internal VLAN Networks on Router0

- VLAN 10 → 192.168.10.0/24
- VLAN 20 → 192.168.20.0/24
- VLAN 30 → 192.168.30.0/24
- VLAN 40 → 192.168.40.0/24
- VLAN 50 → 192.168.50.0/24

---

## EIGRP Configuration Summary

### AS Number

```bash
EIGRP 100

---

## Advertised Networks

Router0:
60.60.60.0/30

Router1:
50.50.50.0/30

Router2:
50.50.50.0/30
60.60.60.0/30

---

## Verification Commands

show ip eigrp neighbors
show ip route
show ip protocols
show ip interface brief
ping

---

## Successful Result

## EIGRP neighbor relationships were successfully established between all routers.

## Dynamic routes were learned correctly, including:

D 50.50.50.0 via 60.60.60.2

This confirms successful route propagation and full routing convergence.

---

## Skills Demonstrated

- Cisco Routing
- EIGRP Protocol
- Dynamic Routing
- Troubleshooting
- Packet Tracer Lab Design
- Network Validation
- Enterprise Routing Concepts

---

Author

GitHub: alhanoofalabdullah-ai

Networking Labs Portfolio Project
