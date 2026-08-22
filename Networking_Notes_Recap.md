# 🌐 Networking Notes – Intermediate

---

## OSI Model

### 1️⃣ Physical Layer
- Hardware and signals.
- Examples: Cables, Hubs.
- Think of it like: The road where cars (data) travel.

### 2️⃣ Data Link Layer
- Ensures correct delivery between two devices.
- Examples: MAC Address, Switches, ARP.
- Think of it like: Traffic police guiding cars.

### 3️⃣ Network Layer
- Decides the path for data.
- Examples: IP Address, ICMP, Routing.
- Think of it like: Google Maps choosing the route.

### 4️⃣ Transport Layer
- Ensures safe delivery.
- Examples: TCP, UDP, 3‑Way Handshake, Ports.
- Think of it like: Courier service ensuring delivery.

### 5️⃣ Session Layer
- Manages conversations.
- Example: Login session on a website.

### 6️⃣ Presentation Layer
- Translates data formats.
- Examples: Encryption, Compression.

### 7️⃣ Application Layer
- The layer we use directly.
- Examples: Browsers, Email apps.

---

## 🔄 TCP/IP vs OSI

| OSI Model (7 Layers) | TCP/IP Model (4 Layers) |
|-----------------------|--------------------------|
| Application           | Application             |
| Presentation          | Application             |
| Session               | Application             |
| Transport             | Transport               |
| Network               | Internet                |
| Data Link             | Network Access          |
| Physical              | Network Access          |

---

## 📦 Encapsulation & De‑encapsulation
- Encapsulation → Wrapping data with headers (Application → Physical).
- De‑encapsulation → Removing headers (Physical → Application).
- Think of it like: Sending a gift (wrap/un‑wrap).

---

## 🔍 Wireshark
- Tool to see network traffic.
- Example: View TCP handshake or IP communication.
- Think of it like: X‑ray vision for your network.

---

## 🖧 IP Addressing & Subnetting

### IPv4
- Format: `192.168.1.1`
