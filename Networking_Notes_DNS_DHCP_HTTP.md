# 🌐 DNS, DHCP & HTTP/HTTPS – Notes

---

## 📡 DNS (Domain Name System)
- **Purpose:** Translates human‑friendly names (e.g., `google.com`) into IP addresses.  
- **Flow:**  
  1. User types a domain in browser.  
  2. DNS resolver queries root → TLD → authoritative server.  
  3. Returns IP address to client.  
- **Example:** `google.com` → `142.250.190.14`.  
- **Think of it like:** A phonebook for the internet.

---

## 🔑 DHCP (Dynamic Host Configuration Protocol)
- **Purpose:** Automatically assigns IP addresses and network settings to devices.  
- **Flow:**  
  1. Device sends **DHCP Discover**.  
  2. Server replies with **Offer**.  
  3. Device sends **Request**.  
  4. Server confirms with **ACK**.  
- **Settings provided:** IP address, subnet mask, gateway, DNS server.  
- **Think of it like:** Reception desk giving you a room number and Wi‑Fi password.

---

## 🌍 HTTP (HyperText Transfer Protocol)
- **Purpose:** Communication protocol for web pages.  
- **Characteristics:**  
  - Plain text, not secure.  
  - Default port: **80**.  
- **Flow:** Client requests → Server responds with HTML.  
- **Limitation:** Data can be intercepted.

---

## 🔒 HTTPS (HTTP Secure)
- **Purpose:** Secure version of HTTP using **SSL/TLS encryption**.  
- **Characteristics:**  
  - Encrypts communication between client and server.  
  - Default port: **443**.  
  - Provides authentication + integrity.  
- **Flow:**  
  1. Client connects to server.  
  2. SSL/TLS handshake establishes encryption keys.  
  3. Secure communication begins.  
- **Think of it like:** Sending a letter in a locked box instead of an open envelope.

---

# 🎯 Quick Recap
- **DNS** → Converts domain names to IP addresses.  
- **DHCP** → Automatically assigns IP + network settings.  
- **HTTP** → Web communication, insecure, port 80.  
- **HTTPS** → Secure web communication, encrypted, port 443.  

---

✅ These protocols form the backbone of how devices connect, identify, and securely communicate on the internet.
