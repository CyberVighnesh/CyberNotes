# 🌐 Network Devices & Protocols – Notes

Networking is built on **devices** that move data and **protocols** that define rules.  
Understanding both gives clarity on how communication flows.

---

## 🖥️ Network Devices

### 🔌 Hub
- **Function:** Basic device that broadcasts data to all connected computers.  
- **Limitation:** No intelligence, causes collisions.  
- **Use Case:** Rare today, replaced by switches.

### 🔗 Switch
- **Function:** Smarter than hubs, forwards data only to the correct device using **MAC addresses**.  
- **Benefit:** Reduces collisions, improves efficiency.  
- **Layer:** Works at **Data Link Layer**.

### 🌍 Router
- **Function:** Connects different networks, decides best path using **IP addresses**.  
- **Benefit:** Enables internet access.  
- **Layer:** Works at **Network Layer**.

### 🛡️ Firewall
- **Function:** Controls traffic based on rules (allow/deny).  
- **Benefit:** Security against unauthorized access.  
- **Layer:** Can operate at multiple layers.

### 📡 Access Point
- **Function:** Provides wireless connectivity (Wi‑Fi).  
- **Benefit:** Extends network without cables.  
- **Layer:** Data Link + Physical.

### 🌐 Gateway
- **Function:** Translates between different protocols/networks.  
- **Example:** VoIP gateway (converts voice to IP packets).

---

## 📜 Protocols

### 📦 TCP (Transmission Control Protocol)
- **Reliable, connection‑oriented.**  
- Uses **3‑way handshake**.  
- Example: Web browsing, email.

### ⚡ UDP (User Datagram Protocol)
- **Fast, connectionless.**  
- No guarantee of delivery.  
- Example: Video streaming, gaming.

### 🌍 IP (Internet Protocol)
- Provides addressing and routing.  
- Versions: **IPv4** (32‑bit) and **IPv6** (128‑bit).

### 🔍 ICMP (Internet Control Message Protocol)
- Used for diagnostics (e.g., **ping**).  
- Helps check connectivity.

### 📧 HTTP/HTTPS
- **Application layer protocols.**  
- HTTP → Web communication.  
- HTTPS → Secure with encryption.

### 📡 DNS (Domain Name System)
- Translates domain names (e.g., `google.com`) into IP addresses.  
- Works like a phonebook for the internet.

### 📤 SMTP / POP3 / IMAP
- **Email protocols:**  
  - SMTP → Sending mail.  
  - POP3 → Downloading mail.  
  - IMAP → Syncing mail across devices.

---

## 🛠️ Tools for Practice

### 🧮 IP Calculator
- Helps calculate subnets, ranges, broadcast addresses.  
- Useful for subnetting exercises.

### 🖥️ Packet Tracer
- Cisco simulation tool.  
- Allows building virtual networks with routers, switches, PCs.  
- Great for practicing protocols and device configurations.

---

# 🎯 Quick Recap
- **Devices:** Hub, Switch, Router, Firewall, Access Point, Gateway.  
- **Protocols:** TCP, UDP, IP, ICMP, HTTP/HTTPS, DNS, Email protocols.  
- **Tools:** IP Calculator, Packet Tracer.  

---

✅ These notes give a **flow from devices → protocols → practice tools**, helping you dig deeper into how networks operate.
