# 🔐 Network Security Basics – Notes

---

## 🛡️ Firewall Types
Firewalls control traffic between networks based on rules.

### Stateless Firewall
- **Checks packets individually** without remembering past traffic.
- Faster, but less secure.
- Example: Simple packet filter.

### Stateful Firewall
- **Tracks connections** (remembers state of traffic).
- More secure, can block abnormal flows.
- Example: Enterprise firewalls.

### Next‑Gen Firewall (NGFW)
- Combines traditional firewall + advanced features.
- Includes **deep packet inspection, intrusion prevention, application awareness**.
- Example: Palo Alto, Fortinet NGFW.

---

## 👀 IDS vs IPS
- **IDS (Intrusion Detection System):**
  - Monitors traffic.
  - Alerts when suspicious activity is detected.
  - Passive (does not block).
- **IPS (Intrusion Prevention System):**
  - Monitors + actively blocks malicious traffic.
  - Inline with network flow.
- **Think of it like:** IDS = CCTV camera, IPS = Security guard.

---

## 🌍 VPN (Virtual Private Network)
Creates a secure tunnel over public networks.

- **IPSec VPN:**
  - Works at network layer.
  - Encrypts IP packets.
  - Used for site‑to‑site secure connections.

- **SSL VPN:**
  - Works at application layer.
  - Uses web browser + SSL/TLS.
  - Common for remote user access.

---

## 🔄 NAT & PAT
- **NAT (Network Address Translation):**
  - Maps private IPs → public IPs.
  - Example: Home router translating `192.168.1.10` → public IP.

- **PAT (Port Address Translation):**
  - Many private IPs share one public IP using different ports.
  - Example: Multiple devices in a home using one internet IP.

---

## 🏰 DMZ (Demilitarized Zone)
- A separate network zone between internal LAN and internet.
- Hosts public‑facing services (web servers, mail servers).
- Provides isolation: if DMZ is compromised, internal LAN stays safe.

---

## 📜 ACL (Access Control List)
- Rules applied on routers/firewalls to permit/deny traffic.
- Works by matching:
  - **Source IP**
  - **Destination IP**
  - **Protocol**
  - **Port number**
- **Detailed Example:**
  - Allow HTTP (port 80) from `192.168.1.0/24` to `10.0.0.5`.
  - Deny all other traffic.
- **Think of it like:** A guest list at an event — only listed people get in.

---

# 🎯 Quick Recap
- **Firewalls:** Stateless, Stateful, NGFW.  
- **IDS vs IPS:** Detect vs prevent.  
- **VPN:** IPSec (network layer), SSL (application layer).  
- **NAT/PAT:** Translate private IPs, share public IPs.  
- **DMZ:** Isolated zone for public servers.  
- **ACL:** Rule‑based traffic control.

---

✅ These notes give a solid foundation in **network security basics** with clear flow and examples.
