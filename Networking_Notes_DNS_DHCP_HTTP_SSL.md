# 🌐 DNS, DHCP & Web Protocols – Notes

---

## 📡 DNS Resolution Process
- **Step 1:** User enters domain (e.g., `example.com`) in browser.
- **Step 2:** Query goes to local DNS resolver (usually ISP).
- **Step 3:** Resolver contacts **Root Server** → points to TLD (.com).
- **Step 4:** Resolver contacts **TLD Server** → points to authoritative server.
- **Step 5:** Authoritative server returns IP address.
- **Step 6:** Resolver caches result and sends IP to client.
- **Step 7:** Browser connects to server using IP.

👉 Flow: Browser → Resolver → Root → TLD → Authoritative → IP → Browser.

---

## 📜 DNS Record Types
- **A Record:** Maps domain → IPv4 address.  
  Example: `example.com → 192.168.1.1`
- **AAAA Record:** Maps domain → IPv6 address.  
  Example: `example.com → 2001:db8::1`
- **MX Record:** Mail exchange server for email delivery.  
  Example: `mail.example.com`
- **CNAME Record:** Alias for another domain.  
  Example: `www.example.com → example.com`
- **PTR Record:** Reverse lookup (IP → domain).  
  Example: `192.168.1.1 → example.com`
- **NS Record:** Specifies authoritative name servers for a domain.

---

## 🔑 DHCP DORA Process
DHCP assigns IP addresses dynamically using **DORA**:

1. **Discover:** Client broadcasts request for IP.  
2. **Offer:** DHCP server offers an IP + settings.  
3. **Request:** Client requests the offered IP.  
4. **ACK:** Server confirms assignment.

👉 Flow: Discover → Offer → Request → ACK.

---

## 🌍 HTTP vs 🔒 HTTPS

| Feature        | HTTP                          | HTTPS                          |
|----------------|-------------------------------|--------------------------------|
| Port           | 80                            | 443                            |
| Security       | No encryption                 | Encrypted via SSL/TLS          |
| Data Safety    | Vulnerable to interception    | Confidential & secure          |
| Use Case       | Basic websites                | Banking, e‑commerce, secure apps |

---

## 🔐 SSL/TLS
- **Purpose:** Provides encryption, authentication, and integrity.  
- **Flow:**  
  1. Client connects to server.  
  2. Server sends certificate (public key).  
  3. Client verifies certificate.  
  4. Keys exchanged → secure channel created.  
  5. Encrypted communication begins.  
- **Think of it like:** Locking your conversation in a secure box only you and the server can open.

---

# 🎯 Quick Recap
- **DNS Resolution:** Domain → IP via resolver, root, TLD, authoritative.  
- **DNS Records:** A, AAAA, MX, CNAME, PTR, NS.  
- **DHCP DORA:** Discover → Offer → Request → ACK.  
- **HTTP vs HTTPS:** Port 80 vs 443, insecure vs secure.  
- **SSL/TLS:** Encryption + authentication for secure communication.
