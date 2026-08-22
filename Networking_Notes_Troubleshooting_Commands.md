# 🛠️ Network Troubleshooting Commands – Notes

---

## 📡 ping
- **Purpose:** Test connectivity to another device.
- **Windows CMD / PowerShell:**  
  `ping google.com`
- **Linux Terminal:**  
  `ping -c 4 google.com`
- **Output:** Shows response time and packet loss.

---

## 🌍 tracert / traceroute
- **Purpose:** Trace the path packets take to a destination.
- **Windows CMD / PowerShell:**  
  `tracert google.com`
- **Linux Terminal:**  
  `traceroute google.com`
- **Output:** Lists each hop (router) along the path.

---

## 🔑 ipconfig / ifconfig
- **Purpose:** Display IP configuration.
- **Windows CMD / PowerShell:**  
  `ipconfig /all`
- **Linux Terminal:**  
  `ifconfig` or `ip addr`
- **Output:** Shows IP, subnet mask, gateway, DNS.

---

## 📖 nslookup
- **Purpose:** Query DNS records.
- **Windows CMD / PowerShell:**  
  `nslookup google.com`
- **Linux Terminal:**  
  `nslookup google.com`
- **Output:** Returns IP address of domain.

---

## 🔍 dig
- **Purpose:** Advanced DNS lookup.
- **Linux Terminal:**  
  `dig google.com`
- **Output:** Detailed DNS records (A, MX, etc.).

---

## 📊 netstat
- **Purpose:** Show active connections and listening ports.
- **Windows CMD / PowerShell:**  
  `netstat -an`
- **Linux Terminal:**  
  `netstat -tulnp`
- **Output:** Displays protocol, local/remote addresses, state.

---

## 🔗 arp
- **Purpose:** Show ARP table (IP ↔ MAC mapping).
- **Windows CMD / PowerShell:**  
  `arp -a`
- **Linux Terminal:**  
  `arp -n`
- **Output:** Lists IP addresses and corresponding MACs.

---

## 🛣️ pathping
- **Purpose:** Combines ping + traceroute for detailed analysis.
- **Windows CMD / PowerShell:**  
  `pathping google.com`
- **Output:** Shows latency and packet loss per hop.

---

## 🗺️ route
- **Purpose:** Display or modify routing table.
- **Windows CMD / PowerShell:**  
  `route print`
- **Linux Terminal:**  
  `route -n` or `ip route`
- **Output:** Shows network routes and gateways.

---

## 💻 hostname
- **Purpose:** Display computer’s hostname.
- **Windows CMD / PowerShell:**  
  `hostname`
- **Linux Terminal:**  
  `hostname`
- **Output:** Shows system name.

---

# 🎯 Quick Recap
- **ping** → Test connectivity.  
- **tracert/traceroute** → Path of packets.  
- **ipconfig/ifconfig** → IP configuration.  
- **nslookup/dig** → DNS queries.  
- **netstat** → Active connections.  
- **arp** → IP ↔ MAC mapping.  
- **pathping** → Latency + packet loss per hop.  
- **route** → Routing table.  
- **hostname** → System name.  

---

✅ These commands are essential for diagnosing and troubleshooting network issues across **Windows CMD, PowerShell, and Linux Terminal**.
