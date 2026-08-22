# 🐧 Linux Essentials – Notes

---

## 📂 1. File System Basics
- **Root (`/`)** → Top of the hierarchy.
- **Home (`/home/user`)** → User files.
- **Bin (`/bin`)** → Essential binaries (commands).
- **Etc (`/etc`)** → Configuration files.
- **Var (`/var`)** → Logs, variable data.
- **Tmp (`/tmp`)** → Temporary files.

---

## 📜 2. Common Commands
- **pwd** → Print working directory.
- **ls** → List files.
- **cd** → Change directory.
- **cp** → Copy files.
- **mv** → Move/rename files.
- **rm** → Remove files.
- **cat** → View file content.
- **nano/vi** → Edit files.
- **chmod** → Change permissions.
- **chown** → Change ownership.

---

## 👤 3. User & Permissions
- **Users & Groups:** Managed via `/etc/passwd` and `/etc/group`.
- **Permissions:**  
  - `r` → Read  
  - `w` → Write  
  - `x` → Execute  
- **Example:** `-rw-r--r--` → Owner can read/write, others can only read.

---

## 🔑 4. Process Management
- **ps** → Show running processes.
- **top/htop** → Monitor system usage.
- **kill** → Terminate process.
- **systemctl** → Manage services.

---

## 🌐 5. Networking Commands
- **ping** → Test connectivity.
- **ifconfig/ip addr** → Show IP configuration.
- **netstat/ss** → Show connections.
- **nslookup/dig** → DNS queries.
- **traceroute** → Path to destination.

---

## 📦 6. Package Management
- **Debian/Ubuntu:** `apt install <package>`
- **RedHat/CentOS:** `yum install <package>` or `dnf install <package>`
- **Arch:** `pacman -S <package>`

---

## 🔒 7. Security Basics
- **sudo** → Run commands as root.
- **ufw/iptables** → Firewall management.
- **ssh** → Secure remote login.
- **passwd** → Change user password.

---

## 🛠️ 8. Shell & Scripting
- **Bash shell:** Default in most distros.
- **Scripts:** Automate tasks with `.sh` files.
- **Example:**
  ```bash
  #!/bin/bash
  echo "Hello, Linux!"         
                                                                                                                       
## 📂 9. Logs & Monitoring
System logs: /var/log/

dmesg: Kernel messages.

journalctl: Systemd logs.

## 🎯 Quick Recap
File system hierarchy → /, /home, /etc, /var.

Commands → ls, cd, cp, mv, rm, cat.

Permissions → rwx for users/groups.

Processes → ps, top, kill.

Networking → ping, ifconfig, traceroute.

Packages → apt, yum, pacman.

Security → sudo, ssh, firewall.

Scripting → Automate with Bash.

Logs → /var/log, journalctl.
