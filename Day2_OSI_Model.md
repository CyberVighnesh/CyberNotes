# 🌐 OSI Model – Notes

The **OSI Model** (Open Systems Interconnection) is like a step‑by‑step guide that explains how computers talk to each other over a network.  
It has **7 layers**, each with its own job.

---

## 1️⃣ Physical Layer
- **What it does:** Deals with actual hardware and signals.
- **Examples:**  
  - Cables (Ethernet cable, fiber optic)  
  - Hubs (simple devices that connect computers)  
- **Think of it like:** The road where cars (data) travel.

---

## 2️⃣ Data Link Layer
- **What it does:** Makes sure data is sent correctly between two devices.  
- **Examples:**  
  - **MAC Address** (unique ID of your computer’s network card)  
  - **Switches** (smarter than hubs, send data only to the right device)  
  - **ARP** (Address Resolution Protocol – finds MAC address from IP address)  
- **Think of it like:** The traffic police guiding cars to the right house.

---

## 3️⃣ Network Layer
- **What it does:** Decides the path data takes.  
- **Examples:**  
  - **IP Address** (like your home address on the internet)  
  - **ICMP** (used for ping – checking if a computer is reachable)  
  - **Routing** (finding the best path for data)  
- **Think of it like:** Google Maps deciding the best route.

---

## 4️⃣ Transport Layer
- **What it does:** Ensures data arrives safely and in order.  
- **Examples:**  
  - **TCP** (reliable, like registered post)  
  - **UDP** (faster, but no guarantee – like normal post)  
  - **3‑Way Handshake** (TCP’s way of saying “Hello, ready?” before sending data)  
  - **Ports** (like doors in a house – e.g., Port 80 for websites, Port 25 for email)  
- **Think of it like:** A delivery service making sure packages arrive correctly.

---

## 5️⃣ Session Layer
- **What it does:** Manages conversations between computers.  
- **Example:** Logging into a website and keeping you connected until you log out.  
- **Think of it like:** A phone call session – starts, continues, ends.

---

## 6️⃣ Presentation Layer
- **What it does:** Translates data into a format both sides understand.  
- **Examples:**  
  - Encryption (locking data for security)  
  - Compression (making files smaller)  
- **Think of it like:** A translator converting languages.

---

## 7️⃣ Application Layer
- **What it does:** The layer we see and use.  
- **Examples:**  
  - Web browsers (Chrome, Edge)  
  - Email apps (Outlook, Gmail)  
- **Think of it like:** The app on your phone that lets you chat, browse, or watch videos.

---

# 🔄 TCP/IP vs OSI Model

| OSI Model (7 Layers) | TCP/IP Model (4 Layers) |
|-----------------------|--------------------------|
| Application           | Application             |
| Presentation          | Application             |
| Session               | Application             |
| Transport             | Transport               |
| Network               | Internet                |
| Data Link             | Network Access          |
| Physical              | Network Access          |

👉 TCP/IP is simpler (4 layers), but OSI is more detailed (7 layers).

---

# 📦 Encapsulation & De‑encapsulation
- **Encapsulation:** Wrapping data with headers as it goes **down** the layers (Application → Physical).  
- **De‑encapsulation:** Removing headers as data goes **up** the layers (Physical → Application).  
- **Think of it like:** Sending a gift – you wrap it in boxes, and the receiver unwraps it.

---

# 🔍 Wireshark
- **What it is:** A free tool to see network traffic.  
- **Use:** Helps you watch how data moves through layers.  
- **Example:** You can see a TCP handshake or check which IP addresses your computer is talking to.  
- **Think of it like:** X‑ray vision for your network.

---

# 🎯 Quick Recap
- Physical → Hardware (cables, hubs)  
- Data Link → MAC, Switches, ARP  
- Network → IP, Routing, ICMP  
- Transport → TCP/UDP, Ports, Handshake  
- Session → Manages conversations  
- Presentation → Encryption, Compression  
- Application → Apps we use (browser, email)  
- TCP/IP vs OSI → 4 vs 7 layers  
- Encapsulation → Wrapping data  
- Wireshark → Tool to see traffic  

---

✅ Read this once, and you’ll have a clear picture of how computers talk in a network.
