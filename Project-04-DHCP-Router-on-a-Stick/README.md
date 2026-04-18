# 🌐 Project-04: DHCP Server with Inter-VLAN Routing

## 📌 Objective

This project demonstrates automatic IP address assignment using DHCP in a multi-VLAN environment with Inter-VLAN routing.

---

## 🧠 Concept

Instead of manually assigning IP addresses, the router acts as a DHCP server and dynamically assigns IPs to devices in different VLANs.

---

## 🏗️ Topology

* 1 Router (Router0)
* 1 Switch (2960)
* 4 PCs
* VLAN 10 (SALES)
* VLAN 20 (HR)

---

## ⚙️ Configuration Summary

### 🔹 Switch

* VLAN 10 & VLAN 20 created
* Ports assigned to VLANs
* Trunk configured to router

### 🔹 Router

* Subinterfaces for VLAN 10 & 20
* DHCP configured for each VLAN
* Gateway addresses assigned

---

## 🌍 IP Addressing

| VLAN | Network      | Gateway      |
| ---- | ------------ | ------------ |
| 10   | 192.168.10.0 | 192.168.10.1 |
| 20   | 192.168.20.0 | 192.168.20.1 |

---

## 🧪 Testing

* Devices automatically received IP addresses ✔️
* Successful communication within VLAN ✔️
* Successful communication between VLANs ✔️

---

## 🚀 Key Learnings

* DHCP configuration
* Dynamic IP assignment
* VLAN + Routing integration
* Network troubleshooting

---

## 🛠️ Tools

* Cisco Packet Tracer

---

## 👩‍💻 Author

Alhanoof Alabdullah
Network & Cloud Engineer 🚀
