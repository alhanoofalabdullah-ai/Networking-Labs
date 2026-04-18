# 🔐 Project 05: VLAN ACL Security

## 📌 Overview
This project demonstrates how to implement Access Control Lists (ACLs) to control traffic between VLANs in a network using Cisco Packet Tracer.

The goal is to allow communication in one direction while restricting it in the opposite direction.

---

## 🧠 Objective
- Configure Inter-VLAN routing using Router-on-a-Stick
- Implement ACL to restrict traffic between VLANs
- Test and verify network security behavior

---

## 🏗️ Network Design
- VLAN 10 → 192.168.10.0/24
- VLAN 20 → 192.168.20.0/24
- Router used for inter-VLAN routing
- Switch configured with trunk port

---

## 🔒 ACL Policy
| Source VLAN | Destination VLAN | Action |
|------------|----------------|--------|
| VLAN 20    | VLAN 10        | ❌ Deny |
| VLAN 10    | VLAN 20        | ✅ Allow |
| Any        | Any            | ✅ Allow |

---

## ⚙️ Configuration Summary
- Subinterfaces created on router:
  - `g0/0/0.10` → VLAN 10
  - `g0/0/0.20` → VLAN 20
- ACL applied inbound on VLAN 20 interface
- Traffic from VLAN 20 to VLAN 10 is blocked

---

## 🧪 Testing Results

### From VLAN 10:
- ✅ Ping VLAN 20 → SUCCESS

### From VLAN 20:
- ❌ Ping VLAN 10 → FAILED (Blocked by ACL)

---

## 📂 Files Included
- `config.txt` → Router configuration
- Packet Tracer topology (optional)

---

## 🚀 Skills Gained
- VLAN segmentation
- Inter-VLAN routing
- ACL implementation
- Network security basics

---
## ⭐ Key Learning
This project highlights how ACLs can enforce security policies in enterprise networks.

## 👩‍💻 Author
**Alhanoof Alabdullah**  
Networking Labs Portfolio 🚀
