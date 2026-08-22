# 🐉 Kali Linux Setup – Notes

---

## 📥 1. Download Kali Linux
- Go to official site: [https://www.kali.org](https://www.kali.org)
- Choose ISO image (64‑bit recommended).
- Verify checksum (SHA256) to ensure integrity.

---

## 💻 2. Installation Options
- **Bare Metal:** Install directly on hardware.
- **Virtual Machine:** Use VMware/VirtualBox.
- **WSL (Windows Subsystem for Linux):** Run inside Windows.
- **Live USB:** Boot without installing, portable option.

---

## ⚙️ 3. Installation Steps
1. Boot from ISO/USB.
2. Select **Graphical Install**.
3. Configure language, keyboard, and region.
4. Set hostname (e.g., `kali`).
5. Create user account + password.
6. Partition disk (guided or manual).
7. Install base system + GRUB bootloader.
8. Reboot into Kali.

---

## 🔑 4. Post‑Installation Setup
- Update system:  
  `sudo apt update && sudo apt upgrade -y`
- Install common tools:  
  `sudo apt install net-tools nmap wireshark metasploit-framework`
- Configure networking:
  - Check IP: `ip addr` or `ifconfig`
  - Test connectivity: `ping google.com`

---

## 🛡️ 5. Security & Customization
- Change default password immediately.
- Enable firewall:  
  `sudo ufw enable`
- Create snapshots if using VM.
- Customize desktop environment (XFCE, GNOME).

---

## 🧰 6. Essential Tools in Kali
- **Nmap:** Network scanning.
- **Wireshark:** Packet analysis.
- **Metasploit:** Exploitation framework.
- **Burp Suite:** Web security testing.
- **Aircrack‑ng:** Wireless security testing.

---

## 🖥️ 7. Integration with Labs
- Use Kali in **Packet Tracer/Virtual Labs** for penetration testing.
- Combine with **routers/switches** to simulate attacks/defenses.
- Practice with **firewall rules, IDS/IPS, VPN setups**.

---

# 🎯 Quick Recap
- Download ISO → Install (bare metal, VM, WSL, Live USB).
- Configure user, hostname, partitions.
- Update + install tools.
- Secure system (passwords, firewall).
- Use Kali for penetration testing, lab simulations, and security research.

---
 
