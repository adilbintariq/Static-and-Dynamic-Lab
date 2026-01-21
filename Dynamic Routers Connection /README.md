# Dynamic Routing and DHCP Configuration Report

## 📌 Project Overview  
This lab demonstrates a multi-router network using **dynamic routing** with the RIP protocol and DHCP services for automatic IP address assignment. The network is built in Cisco Packet Tracer, consisting of four routers connected in a square topology with two WAN links each. Each router provides DHCP services to its local LAN.

---

## 🧱 Network Topology  
- **4 Routers** connected in a square (ring) topology  
- **Serial WAN links** between routers (two per router)  
- **4 separate LANs**, each with multiple PCs receiving IPs via DHCP  
- **Dynamic Routing** using RIP version 2  
- **DHCP pools** configured on each router for automatic IP assignment  

---

## 🖥️ IP Addressing Scheme  

### 🔗 WAN Links (Serial Connections)  

| Link | Network        | IP Addresses       |
|------|----------------|---------------------|
| R1 ↔ R2 | 10.0.0.0/30    | 10.0.0.1 ↔ 10.0.0.2 |
| R2 ↔ R3 | 11.0.0.0/30    | 11.0.0.1 ↔ 11.0.0.2 |
| R3 ↔ R4 | 12.0.0.0/30    | 12.0.0.1 ↔ 12.0.0.2 |
| R4 ↔ R1 | 13.0.0.0/30    | 13.0.0.1 ↔ 13.0.0.2 |

### 🏠 LAN Networks (DHCP Pools)  

| Router | LAN Network     | Gateway          | DHCP Pool         |
|--------|-----------------|------------------|-------------------|
| Router 1 | 220.100.50.0/24 | 220.100.50.1     | 220.100.50.10–254 |
| Router 2 | 220.100.60.0/24 | 220.100.60.1     | 220.100.60.10–254 |
| Router 3 | 220.100.70.0/24 | 220.100.70.1     | 220.100.70.10–254 |
| Router 4 | 220.100.80.0/24 | 220.100.80.1     | 220.100.80.10–254 |

---

## 🧭 Routing Configuration  
- **Dynamic Routing Protocol:** RIP version 2  
- All routers advertise their directly connected networks (LANs and WANs)  
- Each router learns remote routes via RIP updates from neighbors  
- Routing tables are automatically updated when topology changes  

---

## ✅ Verification & Testing  

The following checks were performed:  

✔ All router interfaces are **UP / UP**  
✔ All LAN and WAN networks appear in routing tables as **R (RIP)** routes  
✔ PCs receive IP addresses automatically via **DHCP**  
✔ Successful **ping tests** between PCs across different LANs  
✔ **End-to-end connectivity** confirmed through dynamic routing  

Example from **Router 1’s routing table**:  
- Learned route to `11.0.0.0/8` via `13.0.0.2`  
- Learned route to `12.0.0.0/8` via `10.0.0.2`  
- Both WAN links (`10.0.0.0/30` and `13.0.0.0/30`) are **directly connected**

---

## 🛠 Tools Used  
- Cisco Packet Tracer  
- Cisco IOS CLI  
- RIP (Routing Information Protocol)  
- DHCP Server Configuration  

---

## 🎯 Learning Outcomes  
- Understanding dynamic routing with RIP  
- Configuring DHCP pools on Cisco routers  
- Analyzing routing tables with learned routes  
- Troubleshooting using:  
  - `show ip route`  
  - `show ip interface brief`  
  - `show run | section interface`  

---

## ⚠ Disclaimer  
This project was created for **educational and lab practice purposes only**.  
All IP addresses and configurations are part of a **simulated environment**.

---

## 👤 Author  
**[Muhammad Adil]**  
Networking / Cybersecurity Student  
📍 Packet Tracer | Dynamic Routing | DHCP Configuration | RIP Protocol
