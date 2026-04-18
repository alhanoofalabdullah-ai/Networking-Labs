# 🌐 Project 07: NAT Static Port Forwarding (Web Server)

## 📌 Overview
This project demonstrates **Static NAT (Port Forwarding)** to expose an internal web server to an external network using Cisco Packet Tracer.

The lab simulates a real-world scenario where a private server is published to the public using NAT.

---

## 🎯 Objectives
- Configure Inside and Outside interfaces
- Implement Static NAT (Port Forwarding)
- Allow external users to access internal web server
- Validate connectivity using Ping and HTTP

---

## 🏗️ Network Topology

- Internal Network: `192.168.10.0/24`
- External Network: `200.1.1.0/24`
- Router acts as NAT device
- One internal Web Server
- External client accessing via public IP

---

## ⚙️ Configuration Highlights

### Inside Interface

interface g0/0/0
ip address 192.168.10.1 255.255.255.0
ip nat inside


### Outside Interface

interface g0/0/1
ip address 200.1.1.1 255.255.255.0
ip nat outside


### Static NAT (Port Forwarding)

ip nat inside source static tcp 192.168.10.10 80 200.1.1.1 80


---

## 🌐 Server Configuration

- IP: `192.168.10.10`
- Gateway: `192.168.10.1`
- HTTP Service: Enabled

---

## 🧪 Testing

### Connectivity Test


---

ping 200.1.1.1


### Web Access

http://200.1.1.1


✔️ Successful result:
- External PC can access internal web server

---

## 🧠 Key Concepts Learned

- Network Address Translation (NAT)
- Static NAT vs Dynamic NAT
- Port Forwarding
- Inside / Outside Interfaces
- Real-world Web Publishing

---

## 🚀 Real-World Use Case

This configuration is used in:
- Hosting internal web servers publicly
- Enterprise firewall/NAT setups
- DMZ and secure service exposure

---

## 👩‍💻 Author
**Alhanoof Alabdullah**  
Aspiring Network & Cloud Engineer 🚀

---

## ⭐ Project Status
✔️ Completed  
🔥 Advanced Level Networking Lab

