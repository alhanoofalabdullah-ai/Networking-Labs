# Project 19 — Network Security Monitoring and Threat Detection

Prepared by: Alhanoof Alabdullah

---

## Project Overview

This project demonstrates a professional Network Security Monitoring and Threat Detection environment using Cisco Packet Tracer.

The main objective is to design a secure enterprise network with VLAN segmentation, router-on-a-stick configuration, ACL implementation, protected server access, and security verification using ping tests.

The project focuses on improving network security by isolating departments into separate VLANs and applying Access Control Lists (ACLs) to prevent unauthorized access to sensitive resources such as servers.

This project simulates a real-world enterprise security scenario commonly used in cybersecurity operations, network administration, SOC environments, and infrastructure security engineering.

---

## Project Objectives

* Design a secure segmented network
* Implement VLAN-based isolation
* Configure Router-on-a-Stick inter-VLAN routing
* Protect sensitive servers using ACL
* Block unauthorized access from specific users
* Verify security policies using ping tests
* Simulate enterprise-grade threat detection controls

---

## Network Topology

The network includes:

* 4 Client PCs
* 1 Protected Server
* 2 Cisco Switches
* 2 Cisco Routers
* Multiple VLANs for segmentation

### VLAN Structure

| VLAN ID | Department           | Network         |
| ------- | -------------------- | --------------- |
| 10      | HR Department        | 192.168.10.0/24 |
| 20      | IT Department        | 192.168.20.0/24 |
| 30      | Finance Department   | 192.168.30.0/24 |
| 40      | Admin Department     | 192.168.40.0/24 |
| 50      | Management           | 192.168.50.0/24 |
| 60      | Security Server Zone | 192.168.60.0/24 |

---

## IP Addressing Table

| Device  | IP Address    | Default Gateway |
| ------- | ------------- | --------------- |
| PC0     | 192.168.10.10 | 192.168.10.1    |
| PC1     | 192.168.20.10 | 192.168.20.1    |
| PC2     | 192.168.30.10 | 192.168.30.1    |
| PC3     | 192.168.40.10 | 192.168.40.1    |
| Server0 | 192.168.60.10 | 192.168.60.1    |

---

## Security Policy

### Main Security Rule

PC0 from HR Department:

```text
192.168.10.10
```

is NOT allowed to access:

```text
192.168.60.0/24
```

which contains the protected security server.

### Allowed Access

PC0 is still allowed to access:

* VLAN 20
* VLAN 30
* VLAN 40
* VLAN 50

Only the protected server zone is restricted.

---

## ACL Configuration Logic

### Applied Rule

```text
deny ip host 192.168.10.10 192.168.60.0 0.0.0.255
permit ip any any
```

This ensures:

* Unauthorized access is blocked
* All other traffic remains permitted

This is a common real-world security policy used in:

* SOC operations
* Zero Trust environments
* Internal security segmentation
* Insider threat prevention

---

## Verification Tests

### Test 1 — Blocked Access

From PC0:

```text
ping 192.168.60.10
```

### Result

```text
Destination host unreachable
```

### Status

SUCCESS

---

### Test 2 — Allowed Access

From PC0:

```text
ping 192.168.20.10
```

### Result

```text
Reply from 192.168.20.10
```

### Status

SUCCESS

---

### Test 3 — Allowed Access

From PC0:

```text
ping 192.168.30.10
```

### Result

```text
Reply from 192.168.30.10
```

### Status

SUCCESS

---

## Verification Commands

### Show ACL

```bash
show access-lists
```

### Show Interface Status

```bash
show ip interface brief
```

### Show VLANs

```bash
show vlan brief
```

### Save Configuration

```bash
write memory
```

---

## Skills Demonstrated

* VLAN Configuration
* Trunking
* Access Ports
* Router-on-a-Stick
* Subinterfaces
* ACL Security Rules
* Threat Prevention
* Network Segmentation
* Security Validation
* Enterprise Network Design
* Cybersecurity Controls
* Cisco Packet Tracer Lab Simulation

---

## Business Value

This project reflects how organizations protect critical systems from unauthorized access while maintaining operational communication across departments.

It demonstrates practical implementation of:

* Security Governance
* Internal Threat Prevention
* Department Isolation
* Protected Infrastructure Design

This directly supports enterprise cybersecurity maturity.

---

## Ideal Career Relevance

This project supports roles such as:

* Network Security Engineer
* Cybersecurity Analyst
* SOC Analyst
* Infrastructure Security Engineer
* Security Operations Engineer
* Enterprise Network Engineer
* IT Security Specialist

---

## Repository Structure

```text
project-19-network-security-monitoring-and-threat-detection/
│
├── README.md
├── config.txt
├── topology.png
├── verification-results/
│   ├── ping-tests.png
│   ├── acl-validation.png
│   └── router-validation.png
│
└── project-file/
    └── project19-network-security-monitoring-and-threat-detection.pkt
```

---

## Final Result

Project Successfully Completed

Professional-level enterprise security implementation with real cybersecurity logic and verification.

This is a strong GitHub portfolio project for advanced technical roles.

---

Prepared by: Alhanoof Alabdullah
