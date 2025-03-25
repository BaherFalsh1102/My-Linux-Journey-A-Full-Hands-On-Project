# 📊 Monitoring & Logs in Linux

## ✅ Goal:
Learn how to **monitor system performance, view running processes, and analyze logs** for troubleshooting.

---

## 📌 1️⃣ Monitoring System Performance

### 🔍 Check System Load with `top`
```bash
top
```
- CPU%: Shows CPU usage per process

- MEM%: Displays memory usage

- Press q to quit

### 🔥 Better Alternative: htop (Interactive)
```bash
sudo apt install htop -y   # Ubuntu
htop
```
### 🚀 Check System Resource Usage (free, vmstat)
```bash
free -m          # Check memory usage
vmstat 1 5       # Monitor CPU, memory, and disk usage
```
---
## 📁 2️⃣ Viewing System Logs (journalctl & /var/log/)
### 📖 View System Logs (Journalctl)
```bash
sudo journalctl -xe
```
### 🔍 View Logs for a Specific Service
```bash
sudo journalctl -u sshd --since "1 hour ago"
```
### 📄 Important Log Files
```bash
cat /var/log/syslog      # System logs (Ubuntu)
cat /var/log/auth.log    # Authentication logs
cat /var/log/dmesg       # Kernel logs
```
### 🚀 Monitor Logs in Real-Time (tail -f)
```bash
sudo tail -f /var/log/syslog
```
---
## 📊 3️⃣ Disk & Network Monitoring
### 🗂️ Check Disk Space Usage (df, du)
```bash
df -h            # View disk space usage
du -sh /home     # Check size of a directory
```
### 🌐 Monitor Network Usage (ss, netstat, iftop)
```bash
ss -tulnp        # Show active network connections
sudo iftop       # Monitor real-time bandwidth usage
```
---
## 🛠️ 4️⃣ Automating Monitoring with Scripts
### Create a script system-status.sh:
```bash
#!/bin/bash
echo "System Status Report"
echo "----------------------"
echo "Uptime: $(uptime)"
echo "Memory Usage:"
free -m
echo "Disk Usage:"
df -h
```
**Make it executable and run:**
```bash
chmod +x system-status.sh
./system-status.sh
```

