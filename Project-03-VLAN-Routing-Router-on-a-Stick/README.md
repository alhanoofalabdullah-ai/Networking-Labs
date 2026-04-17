# 🌐 Project-03: Router-on-a-Stick (Inter-VLAN Routing)

## 📌 Objective

This project demonstrates how to enable communication between different VLANs using **Router-on-a-Stick** configuration in Cisco Packet Tracer.

---

## 🧠 Concept

In a typical network, devices in different VLANs cannot communicate directly.
This project solves that by using a router with subinterfaces and trunking to route traffic between VLANs.

---

## 🏗️ Topology

* 1 Router (Router0)
* 1 Switch (2960-24TT)
* 4 PCs
* VLAN 10 (SALES)
* VLAN 20 (HR)

---

## ⚙️ Configuration Summary

### 🔹 Switch

* Created VLAN 10 and VLAN 20
* Assigned access ports to each VLAN
* Configured trunk port to the router

### 🔹 Router

* Configured subinterfaces:

  * `G0/0/0.10` → VLAN 10
  * `G0/0/0.20` → VLAN 20
* Enabled 802.1Q encapsulation
* Assigned IP addresses as gateways

---

## 🌍 IP Addressing

| Device | IP Address   | VLAN | Gateway      |
| ------ | ------------ | ---- | ------------ |
| PC0    | 192.168.10.2 | 10   | 192.168.10.1 |
| PC1    | 192.168.10.3 | 10   | 192.168.10.1 |
| PC2    | 192.168.20.2 | 20   | 192.168.20.1 |
| PC3    | 192.168.20.3 | 20   | 192.168.20.1 |

---

## 🧪 Testing

### ✅ Successful Tests

* PC0 → PC1 (Same VLAN ✔️)
* PC2 → PC3 (Same VLAN ✔️)
* PC0 → PC2 (Different VLAN ✔️ via Router)

### ❌ Before Configuration

* Inter-VLAN communication failed (Request timed out)

---

## 🚀 Key Learnings

* VLAN segmentation
* Trunk configuration (802.1Q)
* Router subinterfaces
* Inter-VLAN routing
* Network troubleshooting using ping

---

## 📷 Screenshots

(Add your Packet Tracer topology and ping results here)

---

## 🛠️ Tools Used

* Cisco Packet Tracer

---

## 👩‍💻 Author

Alhanoof Alabdullah
Aspiring Network & Cloud Engineer 🚀
