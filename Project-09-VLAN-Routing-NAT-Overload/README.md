# 🚀 Project 09 – VLAN Routing with NAT Overload

## 📌 Description
This project demonstrates a layered enterprise network design using **VLAN segmentation**, **Inter-VLAN Routing (Router-on-a-Stick)**, and **NAT Overload (PAT)** in Cisco Packet Tracer.

The topology separates users into different VLANs while allowing controlled communication between networks and external connectivity through a single public IP address.

This project validates practical understanding of:
- VLAN configuration
- Trunking
- Router subinterfaces
- Inter-VLAN communication
- NAT Overload (PAT)
- Network verification and troubleshooting

---

## 🌐 Topology Overview
The network includes:
- 1 Router
- 1 Switch
- 2 PCs in VLAN 10
- 2 PCs in VLAN 20
- 1 External/Public network host

### VLAN Structure
- **VLAN 10** → SALES → `192.168.10.0/24`
- **VLAN 20** → HR → `192.168.20.0/24`

### Public / Outside Network
- `200.1.1.0/24`

---

## 🧠 IP Addressing Plan

### VLAN 10
- PC0 → `192.168.10.10`
- PC1 → `192.168.10.11`
- Default Gateway → `192.168.10.1`

### VLAN 20
- PC2 → `192.168.20.10`
- PC3 → `192.168.20.11`
- Default Gateway → `192.168.20.1`

### Outside Network
- Public Interface → `200.1.1.1`
- Outside PC → `200.1.1.2`

---

## ⚙️ Switch Configuration
```bash
enable
conf t

vlan 10
name SALES

vlan 20
name HR

interface fa0/1
switchport mode access
switchport access vlan 10

interface fa0/2
switchport mode access
switchport access vlan 10

interface fa0/3
switchport mode access
switchport access vlan 20

interface fa0/4
switchport mode access
switchport access vlan 20

interface fa0/24
switchport mode trunk

end
wr

⚙️ Router Configuration

enable
conf t

interface g0/0/0
no ip address
no shutdown

interface g0/0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
ip nat inside

interface g0/0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
ip nat inside

interface g0/0/1
ip address 200.1.1.1 255.255.255.0
ip nat outside
no shutdown

access-list 1 permit 192.168.10.0 0.0.0.255
access-list 1 permit 192.168.20.0 0.0.0.255

ip nat inside source list 1 interface g0/0/1 overload

end
wr

🖥️ End Device Configuration

PC0
IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.10.1
PC1
IP Address: 192.168.10.11
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.10.1
PC2
IP Address: 192.168.20.10
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.20.1
PC3
IP Address: 192.168.20.11
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.20.1
Outside PC
IP Address: 200.1.1.2
Subnet Mask: 255.255.255.0
Default Gateway: 200.1.1.1

🔍 Verification
1. Check VLANs on Switch

show vlan brief

2. Check Trunk Port

show interfaces trunk

3. Verify Router Interfaces

show ip interface brief

4. Test Inter-VLAN Routing

From VLAN 10 host:

ping 192.168.20.10

5. Test External Connectivity

From internal host:

ping 200.1.1.2

6. Verify NAT Translations

show ip nat translations

Expected result:

Private IPs translated to 200.1.1.1
Multiple sessions mapped using different ports/ICMP identifiers
✅ Expected Outcome
Hosts in VLAN 10 can communicate with VLAN 20
Internal devices can reach the external network
NAT Overload translates internal traffic using one public IP
Trunk link carries VLAN traffic correctly between switch and router
💡 Key Networking Concepts
VLAN Segmentation
Access Ports
Trunk Ports
Router-on-a-Stick
Subinterfaces
NAT Overload / PAT
Inter-VLAN Routing
Enterprise Layer 2 / Layer 3 integration
🏁 Conclusion

This project demonstrates a practical enterprise-style implementation combining VLANs, trunking, inter-VLAN routing, and NAT Overload. It highlights the ability to design, configure, verify, and troubleshoot a multi-network topology using Cisco Packet Tracer.

🔥 Tagline

Segment. Route. Translate. Connect.


# config.txt
```text
enable
conf t

vlan 10
name SALES

vlan 20
name HR

interface fa0/1
switchport mode access
switchport access vlan 10

interface fa0/2
switchport mode access
switchport access vlan 10

interface fa0/3
switchport mode access
switchport access vlan 20

interface fa0/4
switchport mode access
switchport access vlan 20

interface fa0/24
switchport mode trunk

exit

interface g0/0/0
no ip address
no shutdown

interface g0/0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
ip nat inside

interface g0/0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
ip nat inside

interface g0/0/1
ip address 200.1.1.1 255.255.255.0
ip nat outside
no shutdown

access-list 1 permit 192.168.10.0 0.0.0.255
access-list 1 permit 192.168.20.0 0.0.0.255

ip nat inside source list 1 interface g0/0/1 overload

end
wr

