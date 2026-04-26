# Project 13 – OSPF Multi-Area Enterprise Network

## Overview

This project demonstrates an enterprise network using OSPF (Open Shortest Path First) with multiple routers, VLAN segmentation, and dynamic routing across the network.

The topology includes:

* Core Router (Router0)
* Branch Router 1 (Router1)
* Branch Router 2 (Router2)
* Layer 2 Switch
* Multiple PCs
* Server

The main objective is to establish full connectivity between all VLANs and remote networks using OSPF dynamic routing.

---

## Network Topology

### Router Connections

| Device  | Interface | IP Address    |
| ------- | --------- | ------------- |
| Router0 | G0/0/1    | 10.10.10.1/30 |
| Router1 | G0/0      | 10.10.10.2/30 |
| Router0 | G0/0/0    | 20.20.20.1/30 |
| Router2 | G0/0      | 20.20.20.2/30 |

---

## VLAN Networks

| VLAN    | Network         |
| ------- | --------------- |
| VLAN 10 | 192.168.10.0/24 |
| VLAN 20 | 192.168.20.0/24 |
| VLAN 30 | 192.168.30.0/24 |
| VLAN 40 | 192.168.40.0/24 |
| VLAN 50 | 192.168.50.0/24 |

---

## OSPF Configuration

### Router0

```bash
enable
conf t

router ospf 1
network 10.10.10.0 0.0.0.3 area 0
network 20.20.20.0 0.0.0.3 area 0
network 192.168.10.0 0.0.0.255 area 0
network 192.168.20.0 0.0.0.255 area 0
network 192.168.30.0 0.0.0.255 area 0
network 192.168.40.0 0.0.0.255 area 0
network 192.168.50.0 0.0.0.255 area 0

end
wr
```

---

### Router1

```bash
enable
conf t

interface g0/0
ip address 10.10.10.2 255.255.255.252
no shutdown

router ospf 1
network 10.10.10.0 0.0.0.3 area 0

end
wr
```

---

### Router2

```bash
enable
conf t

interface g0/0
ip address 20.20.20.2 255.255.255.252
no shutdown

router ospf 1
network 20.20.20.0 0.0.0.3 area 0

end
wr
```

---

## Verification Commands

### Check OSPF Neighbors

```bash
show ip ospf neighbor
```

---

### Check Routing Table

```bash
show ip route
```

---

### Test Connectivity

```bash
ping 192.168.50.2
```

Successful Result:

```bash
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
```

---

## Final Result

* OSPF neighbors established successfully
* Full routing table learned dynamically
* End-to-end connectivity verified
* Enterprise network fully operational

---

## Skills Demonstrated

* OSPF Routing
* VLAN Segmentation
* Router-on-a-Stick
* Enterprise Network Design
* Cisco Packet Tracer
* Network Troubleshooting
* Routing Verification

---

## Author

### Alhanoof Alabdullah

Senior Digital Transformation & Enterprise Systems Specialist
PMIS | Network Infrastructure | Enterprise Solutions | Digital Governance
