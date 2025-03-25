# 🌐 Linux Networking Basics

## ✅ Goal:
Understand how to configure network interfaces, check connectivity, and troubleshoot network issues in Linux.

---

## 🔧 Tools & Commands:
- `ip`, `ifconfig`, `nmcli`
- `ping`, `traceroute`, `netstat`, `ss`
- `nslookup`, `dig`

---

## 🧑‍🔧 1️⃣ Checking Network Interfaces

### 🔍 Show All Network Interfaces
```bash
ip a
#or (older method):
ifconfig -a
```
### 🔍 Show Active Network Interfaces
```bash
ip link show
```
---

## 📡 2️⃣ Configuring an IP Address
### 📝 Assign a Static IP (Temporarily)
```bash
sudo ip addr add 192.168.1.100/24 dev eth0
```
### 📝 Assign a Static IP (Permanent – Ubuntu Example)
```bash
sudo nmcli connection modify "Wired connection 1" ipv4.addresses 192.168.1.100/24
#then apply the changes:
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"
```
---
## 🌍 3️⃣ Checking Network Connectivity
### 🏓 Ping a Website
```bash
ping -c 4 google.com
```
### 📡 Check Routing Table
```bash
ip route show
```
### 🔄 Trace Network Route
```bash
traceroute google.com
```
### 🕵️‍♂️ DNS Lookup
```bash
nslookup google.com
dig google.com
```
---
## 🔐 4️⃣ Firewall & Port Checking
### 📖 List Open Ports
```bash
netstat -tulnp
ss -tulnp
```
### 🔥 Check Firewall Status (Ubuntu Example)
```bash
sudo ufw status
```
### 🚪 Allow SSH (Port 22)
```bash
sudo ufw allow 22/tcp
sudo ufw enable
```
