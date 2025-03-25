# 📦 Package Management & Bash Scripting

## ✅ Goal:
Learn how to manage software packages using **apt, yum, dnf** and automate tasks with **Bash scripting**.

---

## 📌 1️⃣ Managing Packages in Linux
### 📖 Check Installed Packages
#### ✅ Debian-based (Ubuntu)
```bash
dpkg -l | grep apache2
```
### 📥 Installing Packages
**✅ Ubuntu (APT)**
```bash
sudo apt update
sudo apt install nginx -y
```
**✅ CentOS (YUM)**
```bash
sudo yum install nginx -y
```
### 🔄 Updating & Removing Packages
```bash
sudo apt upgrade -y         # Ubuntu
sudo yum update -y          # CentOS
sudo dnf upgrade -y         # Fedora

sudo apt remove nginx -y    # Remove package (Ubuntu)
sudo yum remove nginx -y    # Remove package (CentOS)
```
---
## 🤖 2️⃣ Automating Tasks with Bash Scripting
### 📄 Creating a Simple Bash Script
```bash
#!/bin/bash
echo "Hello, $USER! Today is $(date)."
# Save the file as hello.sh and make it executable:
chmod +x hello.sh
./hello.sh
```
---
## 🚀 3️⃣ Writing a System Update Script
### 📄 Creating a Simple Bash Script
**a script named `update-system.sh` has created**
```bash
#!/bin/bash
echo "Updating system..."
sudo apt update && sudo apt upgrade -y
echo "System update completed!"
# Make it executable and run:
chmod +x update-system.sh
./update-system.sh
```
---
## 🛠️ 4️⃣ Automating Backups with Crontab
### 📂 Backup a Directory Every Day
**a script named `backup.sh` has created**
```bash
#!/bin/bash
tar -czf /backup/home-$(date +%F).tar.gz /home
```
### ⏲️ Schedule it with Crontab
```bash
crontab -e
```
**Add the following line to run it every day at midnight:**
```bash
0 0 * * * /path/to/backup.sh
```

