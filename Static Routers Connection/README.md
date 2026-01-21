# Packet Tracer Static Routing – Multi-Router Network

## 📌 Project Overview

This project demonstrates a multi-router network topology built and configured in Cisco Packet Tracer, focusing on static routing, proper IP addressing, and end-to-end connectivity between multiple LANs.

The lab uses four routers connected via serial WAN links, with each router serving a separate LAN through a switch and end devices.

## 🧱 Network Topology

- **4 Routers** connected in a linear (chain) topology
- **Serial point-to-point WAN links** between routers
- **4 separate LANs**, each connected via a switch
- **Static routing** configured on all routers
- 📷 **Topology diagram** included in the repository

## 🖥️ IP Addressing Scheme

### 🔗 WAN Links

| Link | Network | IP Addresses |
|------|---------|--------------|
| R1 ↔ R2 | 10.0.0.0/8 | 10.0.0.1 ↔ 10.0.0.2 |
| R2 ↔ R3 | 11.0.0.0/8 | 11.0.0.1 ↔ 11.0.0.2 |
| R3 ↔ R4 | 12.0.0.0/8 | 12.0.0.1 ↔ 12.0.0.2 |

### 🏠 LAN Networks

| Router | LAN Network | Gateway |
|--------|-------------|---------|
| Router 1 | 192.168.1.0/24 | 192.168.1.1 |
| Router 2 | 192.168.2.0/24 | 192.168.2.1 |
| Router 3 | 192.168.3.0/24 | 192.168.3.1 |
| Router 4 | 192.168.4.0/24 | 192.168.4.1 |

## 🧭 Routing Configuration

- Static routes are **manually configured** on each router
- Each router forwards traffic to remote LANs using the appropriate **next-hop serial IP**
- **No dynamic routing protocols** are used

This approach helps in understanding:
- Route selection
- Next-hop logic
- Manual network control

## ✅ Verification & Testing

The following checks were performed:

✔ All router interfaces are **UP / UP**  
✔ All LAN networks appear in routing tables  
✔ Successful **ICMP (ping)** between PCs across different LANs  
✔ **End-to-end connectivity** confirmed

## 🛠 Tools Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Static Routing

## 🎯 Learning Outcomes

- Understanding static routing concepts
- Hands-on experience with multi-router networks
- IP addressing and subnet planning
- WAN serial link configuration
- Troubleshooting using `show ip route` and `show ip interface brief`

## ⚠ Disclaimer

This project was created for **educational and lab practice purposes only**.  
All IP addresses and configurations are part of a **simulated environment**.

## 👤 Author

**[ Muhammad Adil ]**  
Networking / Cybersecurity Student  
📍 Packet Tracer | Routing | Networking Fundamentals