# 🔐 Linux Security: Firewalls, Fail2ban, and SELinux

## ✅ Goal:
Learn how to secure a Linux system using **firewalls (UFW & iptables)**

---
## 🔥Configuring the Firewall (UFW & iptables)
### 📖 Check Firewall Status
#### ✅ UFW (Ubuntu/Debian)
```bash
sudo ufw status
```
### 🚪 Allow or Deny Ports with UFW (Ubuntu)
```bash
sudo ufw allow 22/tcp     # Allow SSH
sudo ufw allow 80/tcp     # Allow HTTP
sudo ufw enable           # Activate Firewall
```
### 🔄 Iptables: Block an IP (Manually)
```bash
sudo iptables -A INPUT -s 192.168.1.100 -j DROP
```
