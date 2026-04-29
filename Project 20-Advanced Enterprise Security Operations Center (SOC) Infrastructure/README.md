# Project 20 — Advanced Enterprise Security Operations Center (SOC) Infrastructure

## Author

Prepared by: Alhanoof Alabdullah

---

## Project Overview

This project demonstrates a professional Enterprise Security Operations Center (SOC) infrastructure using Cisco Packet Tracer.

The objective is to simulate a real-world enterprise cybersecurity environment where security monitoring, access control, segmentation, and threat mitigation are implemented across multiple departments and critical systems.

This project includes:

- Core Router Infrastructure
- Layer 2 & Layer 3 Switching
- VLAN Segmentation
- ACL Security Policies
- Secure Server Zone
- SOC Monitoring Server
- Firewall Logic using ACLs
- Threat Isolation Mechanism
- Secure Management Access
- Internal Department Separation
- Controlled Inter-VLAN Communication
- Security Event Logging Design

This lab reflects enterprise-grade SOC architecture used in:

- Banks
- Government Facilities
- Oil & Gas Companies
- Smart Cities
- Defense Organizations
- Data Centers
- Critical Infrastructure Projects

---

## Project Objectives

### Main Goals

- Build a secure enterprise network
- Separate departments using VLANs
- Protect critical servers
- Control unauthorized access
- Implement ACL-based firewall policies
- Simulate security monitoring operations
- Restrict lateral movement
- Protect sensitive data
- Improve threat visibility
- Apply real-world cybersecurity architecture

---

## Network Topology

### Departments

| Department | VLAN | Network |
|---|---:|---|
| HR Department | VLAN 10 | 192.168.10.0/24 |
| Finance Department | VLAN 20 | 192.168.20.0/24 |
| IT Department | VLAN 30 | 192.168.30.0/24 |
| Security Department | VLAN 40 | 192.168.40.0/24 |
| SOC Monitoring | VLAN 50 | 192.168.50.0/24 |
| Secure Server Zone | VLAN 60 | 192.168.60.0/24 |
| Management VLAN | VLAN 99 | 192.168.99.0/24 |

---

## Devices Used

### Network Devices

- 2 Routers (Cisco 2911)
- 3 Switches (Cisco 2960)
- 1 SOC Monitoring Server
- 1 Secure Application Server
- 8 PCs
- Admin Management PC
- Security Analyst PC

---

## IP Addressing Plan

| Device | IP Address |
|---|---|
| Router Gateway VLAN 10 | 192.168.10.1 |
| Router Gateway VLAN 20 | 192.168.20.1 |
| Router Gateway VLAN 30 | 192.168.30.1 |
| Router Gateway VLAN 40 | 192.168.40.1 |
| Router Gateway VLAN 50 | 192.168.50.1 |
| Router Gateway VLAN 60 | 192.168.60.1 |
| Router Gateway VLAN 99 | 192.168.99.1 |
| SOC Server | 192.168.50.10 |
| Secure Server | 192.168.60.10 |
| Admin PC | 192.168.99.10 |

---

## Security Policies Implemented

### Access Control Policies

### Rule 1

HR cannot access Finance directly

### Rule 2

Only Security Department can access SOC Server

### Rule 3

Only Management VLAN can SSH/Telnet to network devices

### Rule 4

Only IT Department can access Secure Application Server

### Rule 5

Finance cannot access Secure Server Zone

### Rule 6

Threat traffic is blocked using ACL filtering

### Rule 7

Unauthorized ping requests are denied

### Rule 8

Only approved VLANs can communicate with Server Zone

---

## Router Security Features

### Enabled Security Controls

- Extended ACLs
- Standard ACLs
- Interface-based Filtering
- Subinterfaces
- Inter-VLAN Routing
- Secure Management Access
- SSH Access Logic
- VLAN Trunking
- Port Security Design
- Threat Segmentation

---

## Verification Commands

### Router Commands

```bash
show ip interface brief
show access-lists
show running-config
show vlan brief
show interfaces trunk
show mac address-table
show arp
show ip route
ping
traceroute

----------------

## Testing Scenarios

- Successful Tests
- IT → Secure Server = SUCCESS
- Security → SOC Server = SUCCESS
- Management → Switch Access = SUCCESS

------------------------------

## Router → All VLANs = SUCCESS

- Blocked Tests
- HR → Finance = BLOCKED
- Finance → Secure Server = BLOCKED
- Random PC → SOC Server = BLOCKED
- Unauthorized Device → Management Access = BLOCKED

---------------------------------

## Real-World Use Cases

## This architecture is suitable for:

- SIEM Deployment Labs
- SOC Team Training
- Cybersecurity Audits
- Internal Penetration Testing
- Zero Trust Network Design
- Enterprise Security Architecture
- Critical Infrastructure Protection
- Compliance Validation
- Threat Hunting Practice

------------------------------------

## Skills Demonstrated

- Networking Skills
- VLAN Design
- Trunk Configuration
- Router-on-a-Stick
- Layer 2 Security
- Layer 3 Security

------------------------------------

## Cybersecurity Skills

- ACL Security
- Segmentation Strategy
- Threat Isolation
- Server Protection
- Access Restriction
- Monitoring Infrastructure
- SOC Design Principles

------------------------------------

## Professional Skills

- Enterprise Documentation
- Security Architecture Planning
- Incident Prevention Design
- Operational Security Strategy

-------------------------------------

## GitHub Repository Structure

project-20-advanced-enterprise-soc/
│
├── README.md
├── config.txt

----------------------------------------

## Final Notes

## This project is designed to represent a high-level professional cybersecurity portfolio project suitable for:

- Cybersecurity Engineers
- SOC Analysts
- Network Security Engineers
- Infrastructure Security Specialists
- Enterprise Security Architects
- Digital Transformation Security Teams

-------------------------------------------

Author :

Alhanoof Alabdullah
