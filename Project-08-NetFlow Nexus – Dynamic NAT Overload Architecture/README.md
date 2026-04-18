# 🚀 NetFlow Nexus – Dynamic NAT Overload Architecture

---

## 📌 Description

This project demonstrates a **Dynamic NAT (PAT Overload)** implementation using Cisco Packet Tracer.

It simulates a real-world enterprise scenario where multiple internal devices share a **single public IP address** to access external networks.

---

## 🌐 Topology Overview

* Router (NAT configured)
* Switch (Layer 2)
* Internal PCs (Private Network)
* External PC (Public Network)
* Server (Optional internal resource)

---

## 🧠 Network Design

### 🔹 Inside Network

```
192.168.10.0/24
```

### 🔹 Outside Network

```
200.1.1.0/24
```

---

## ⚙️ Configuration

### 🖥️ Router

```
enable
conf t

interface g0/0/0
ip address 192.168.10.1 255.255.255.0
ip nat inside
no shutdown

interface g0/0/1
ip address 200.1.1.1 255.255.255.0
ip nat outside
no shutdown

access-list 1 permit 192.168.10.0 0.0.0.255

ip nat inside source list 1 interface g0/0/1 overload

end
wr
```

---

### 💻 PCs

#### PC0

```
IP: 192.168.10.10
Mask: 255.255.255.0
Gateway: 192.168.10.1
```

#### PC1

```
IP: 192.168.10.11
Mask: 255.255.255.0
Gateway: 192.168.10.1
```

#### PC2 (Public)

```
IP: 200.1.1.2
Mask: 255.255.255.0
Gateway: 200.1.1.1
```

---

## 🔍 Verification

### ✅ Test Gateway

```
ping 192.168.10.1
```

✔️ Success

---

### ✅ Test External Connectivity

```
ping 200.1.1.2
```

✔️ First ping may fail (normal)
✔️ Then successful replies

---

### ✅ Check NAT

```
show ip nat translations
```

---

## 🧪 Expected Behavior

* Multiple internal devices use **one public IP**
* NAT dynamically assigns ports (PAT)
* Traffic flows successfully to external network

---

## 💡 Key Concepts

* NAT (Network Address Translation)
* PAT (Port Address Translation)
* Inside vs Outside interfaces
* ACL configuration
* IP optimization

---

## 🏁 Conclusion

This project validates a real-world NAT Overload deployment and demonstrates core networking and troubleshooting skills.

---

## 🔥 Tagline

> One IP. Unlimited Access. Intelligent Translation.
