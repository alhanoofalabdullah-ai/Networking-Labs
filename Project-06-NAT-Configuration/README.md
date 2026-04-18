# 🌐 Project-06: NAT Configuration

This project demonstrates Network Address Translation (NAT) using Cisco Packet Tracer.  
The goal is to allow internal private IP addresses to communicate with an external network using a public IP.

---

## 🎯 Objectives
- Configure NAT (PAT - Overload)
- Allow internal LAN to access external network
- Understand inside and outside interfaces

---

## 🧱 Network Topology
- 4 PCs (Internal Network)
- 1 Switch
- 1 Router
- 1 External Network (Simulated)

---

## 🌍 IP Addressing

### Internal Network
- Network: `192.168.10.0/24`
- Gateway: `192.168.10.1`

### External Network
- Network: `200.1.1.0/24`
- Router Interface: `200.1.1.1`

---

## ⚙️ Configuration Summary

- Inside Interface: `GigabitEthernet0/0`
- Outside Interface: `GigabitEthernet0/1`
- NAT Type: PAT (Overload)

---

## 🧪 Testing

### Successful Tests:
- Ping from PC to Router (Internal) ✅
- Ping from PC to External Interface (200.1.1.1) ✅
- Ping to external host (200.1.1.2) ✅

> Note: First ping may fail due to ARP resolution (normal behavior).

---

## 🚀 Key Commands Used
- `ip nat inside`
- `ip nat outside`
- `access-list`
- `ip nat inside source list ... overload`

---

## 💡 What I Learned
- Difference between inside and outside interfaces
- How NAT translates private IP to public IP
- Basic troubleshooting using ping

---

## 📁 Files Included
- Packet Tracer file (.pkt)
- Configuration file (config.txt)

---

## 👩‍💻 Author
Alhanoof Alabdullah
