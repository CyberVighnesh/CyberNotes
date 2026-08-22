# 🌐 Advanced Subnetting & IPv6 – Notes

Networking goes beyond basic IPs and masks.  
Here we explore **VLSM, Supernetting, IPv6, and transition techniques**.

---

## 🔢 VLSM (Variable Length Subnet Mask)
- **What it is:** Allows using different subnet masks within the same network.  
- **Why:** Efficient use of IP addresses.  
- **Example:**  
  - Network: `192.168.1.0/24`  
  - Divide into:  
    - `/26` → 64 addresses (for large group)  
    - `/28` → 16 addresses (for small group)  
- **Flow:** Start with the largest subnet → allocate → move to smaller ones.

---

## 🛠️ Supernetting
- **What it is:** Opposite of subnetting – combines smaller networks into one larger block.  
- **Why:** Reduces routing table size.  
- **Example:**  
  - Four networks: `192.168.0.0/24`, `192.168.1.0/24`, `192.168.2.0/24`, `192.168.3.0/24`  
  - Supernet: `192.168.0.0/22`  
- **Flow:** Merge contiguous networks → advertise as one.

---

## 🌍 IPv6 Addressing
- **Why IPv6:** IPv4 is limited (~4.3 billion addresses). IPv6 provides **340 undecillion** addresses.  
- **Format:** Hexadecimal, 128 bits.  
  - Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
- **Shortening rules:**  
  - Remove leading zeros → `2001:db8:85a3::8a2e:370:7334`  
- **Types:**  
  - **Unicast** → One‑to‑one communication  
  - **Multicast** → One‑to‑many  
  - **Anycast** → One‑to‑nearest  

---

## 🔄 IPv4 vs IPv6

| Feature        | IPv4                        | IPv6                          |
|----------------|-----------------------------|--------------------------------|
| Address size   | 32 bits (e.g., 192.168.1.1) | 128 bits (e.g., 2001:db8::1)   |
| Format         | Decimal, dotted             | Hexadecimal, colon separated   |
| Addresses      | ~4.3 billion                | ~340 undecillion               |
| Config         | Manual / DHCP               | Auto‑configuration supported   |
| Security       | Optional (IPSec)            | Built‑in (mandatory IPSec)     |

---

## ⚙️ Dual Stack
- **What it is:** Devices run both IPv4 and IPv6 simultaneously.  
- **Why:** Smooth transition from IPv4 to IPv6.  
- **Flow:**  
  - Device has two addresses → communicates depending on peer support.  
- **Example:** A router with `192.168.1.1` (IPv4) and `2001:db8::1` (IPv6).

---

## 🌉 Tunneling
- **What it is:** Encapsulating IPv6 packets inside IPv4 to travel across IPv4 networks.  
- **Why:** Helps IPv6 traffic move through legacy IPv4 infrastructure.  
- **Types:**  
  - **6to4** → Automatic tunneling using IPv4 public addresses.  
  - **Teredo** → Works even behind NAT.  
  - **GRE tunnels** → Manual setup for secure paths.  
- **Flow:** IPv6 packet → wrapped in IPv4 → sent → unwrapped at destination.

---

# 🎯 Quick Recap
- **VLSM** → Efficient subnetting with variable masks.  
- **Supernetting** → Combine networks to simplify routing.  
- **IPv6** → Huge address space, new format, built‑in security.  
- **IPv4 vs IPv6** → Key differences in size, format, and features.  
- **Dual Stack** → Run both IPv4 and IPv6 together.  
- **Tunneling** → Carry IPv6 traffic over IPv4 networks.  

---

✅ These notes dig deeper into subnetting and IPv6 transition methods, giving a clear flow for intermediate learners.
