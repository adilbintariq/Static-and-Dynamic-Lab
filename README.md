# 📁 Network Routing Labs – Static vs. Dynamic

This repository contains two hands-on networking labs built in **Cisco Packet Tracer**, each demonstrating a different approach to routing in a multi-router environment.

---

## 📂 Lab 1 – **Static Routing**
**Folder:** `static-routing-lab`  
A manual routing setup where all routes are configured by hand. This lab focuses on control, precision, and understanding the basics of IP forwarding.

### 🔧 Key Features:
- Linear topology with 4 routers
- Static route configuration
- Manual IP assignment
- Full connectivity between LANs

### 📌 Use Case:
Ideal for learning how routing tables are built manually and how traffic flows between networks without automation.

---

## 📂 Lab 2 – **Dynamic Routing with DHCP**
**Folder:** `dynamic-routing-dhcp-lab`  
An automated network using **RIP version 2** for dynamic routing and **DHCP** for automatic IP address assignment.

### 🔧 Key Features:
- Square (ring) topology for redundancy
- RIP dynamic routing protocol
- DHCP pools on each router
- Automatic route learning and failover capability

### 📌 Use Case:
Great for understanding how networks scale, automate, and self-heal using dynamic protocols and services.

---

## 🎯 Learning Comparison

| Aspect | Static Routing Lab | Dynamic Routing + DHCP Lab |
|--------|-------------------|----------------------------|
| **Routing Method** | Manual static routes | RIP dynamic routing |
| **IP Assignment** | Manual | DHCP automatic |
| **Topology** | Linear (chain) | Square (ring) |
| **Config Complexity** | Higher per router | Higher initial setup |
| **Scalability** | Low | High |
| **Real-world Use** | Small networks, default routes | Medium to large networks |

---

## 🚀 How to Use
1. Open **Cisco Packet Tracer**
2. Load the `.pkt` file from the desired lab folder
3. Explore the configurations using the CLI on each router
4. Test connectivity using `ping` between PCs
5. Compare routing tables with `show ip route`

---

## 📎 Files Included
- `static-routing-lab/` – Static routing lab files
- `dynamic-routing-dhcp-lab/` – Dynamic routing with DHCP lab files
- `README.md` – This file

---

## 👤 Author
**Muhammad Adil**  
Networking & Cybersecurity Student  
📍 Cisco Packet Tracer | Routing Protocols | Network Automation

---
