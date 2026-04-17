# Project 02 - VLAN

## Objective
Segment the network into two VLANs and control communication between devices.

## VLAN Configuration
- VLAN 10: PC0, PC1
- VLAN 20: PC2, PC3

## IP Addressing
- PC0: 192.168.1.1
- PC1: 192.168.1.2
- PC2: 192.168.1.3
- PC3: 192.168.1.4

## Configuration Steps
- Created VLAN 10 and VLAN 20
- Assigned switch ports to each VLAN
- Verified connectivity within VLAN
- Verified isolation between VLANs

## Test Results
- PC0 → PC1 ✅ Success
- PC0 → PC2 ❌ Failed (VLAN isolation)

## Result
Network successfully segmented using VLANs.

## Tools Used
- Cisco Packet Tracer
