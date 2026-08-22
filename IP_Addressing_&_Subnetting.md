# 🌐 IP Addressing & Subnetting – Notes

Networking is like sending letters between houses.  
Each computer needs an **address** (IP) and rules (subnetting) to know where to send data.

---

## 🖥️ Physical Layer
- **What it does:** Hardware and signals.
- **Examples:**  
  - Cables (Ethernet, Fiber)  
  - Hubs (basic connectors)  
- **Think of it like:** The actual roads where cars (data) travel.

---

## 🔗 Data Link Layer
- **What it does:** Ensures correct delivery between two devices.
- **Examples:**  
  - **MAC Address** (unique ID of your device)  
  - **Switches** (send data only to the right device)  
  - **ARP** (finds MAC address from IP address)  
- **Think of it like:** Traffic police guiding cars to the right house.

---

## 🌍 Network Layer
- **What it does:** Decides the path for data.
- **Examples:**  
  - **IP Address** (like your home address)  
  - **ICMP** (ping – check if reachable)  
  - **Routing** (best path for data)  
- **Think of it like:** Google Maps choosing the route.

---

## 📦 Transport Layer
- **What it does:** Makes sure data arrives safely.
- **Examples:**  
  - **TCP** (reliable, like registered post)  
  - **UDP** (fast, but no guarantee – like normal post)  
  - **3‑Way Handshake** (TCP’s “Hello, ready?” process)  
  - **Ports** (doors in a house – e.g., Port 80 for websites)  
- **Think of it like:** A courier service ensuring delivery.

---

## 🔢 IP Addressing
- **IPv4:** Written as four numbers (e.g., `192.168.1.1`)  
- **IPv6:** Longer format for more devices (e.g., `2001:db8::1`)  
- **Public IP:** Used on the internet.  
- **Private IP:** Used inside homes/offices (e.g., `192.168.x.x`).  
- **Think of it like:** Street addresses – public is citywide, private is inside your colony.

---

## 📏 Subnetting
- **What it does:** Divides a big network into smaller parts.  
- **Subnet Mask:** Defines how many devices fit in a network.  
  - Example: `255.255.255.0` → allows 254 devices.  
- **CIDR Notation:** `/24` means 24 bits for network, rest for devices.  
- **Think of it like:** Dividing a big apartment building into smaller flats.

---

## 🧮 IP Calculator
- Helps calculate:  
  - Network address  
  - Broadcast address  
  - Number of usable IPs  
- **Example:**  
  - IP: `192.168.1.10/24`  
  - Network: `192.168.1.0`  
  - Broadcast: `192.168.1.255`  
  - Usable: `192.168.1.1 – 192.168.1.254`

---

## 🛠️ Packet Tracer
- **What it is:** A simulation tool by Cisco.  
- **Use:** Practice networking without real devices.  
- **Example:** You can connect virtual PCs, routers, and switches to see how data flows.  
- **Think of it like:** A video game for learning networking.

---

# 🎯 Quick Recap
- Physical → Hardware (cables, hubs)  
- Data Link → MAC, Switches, ARP  
- Network → IP, Routing, ICMP  
- Transport → TCP/UDP, Ports, Handshake  
- IP Address → Device identity (public/private)  
- Subnetting → Divide networks into smaller parts  
- IP Calculator → Helps find ranges  
- Packet Tracer → Practice networking virtually  

---

✅ Read this once, and you’ll understand the basics of IP Addressing & Subnetting.
