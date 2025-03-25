# 👥 Users, Groups & Permissions

## ✅ Goal:
Learn how to create and manage users, set permissions, and control file access using groups and permissions.

---

## 🔧 Tools
- `useradd`, `passwd`, `usermod`, `groupadd`
- `chmod`, `chown`, `chgrp`
- `ls -l`

---

## 🧑‍🔧 Common Commands
```bash
### 👤 Create a User
sudo useradd -m Baher_H
sudo passwd Baher_H

### 👨‍👩‍👧‍👦 Create a Group
sudo groupadd devs

### Add User to Group
sudo usermod -aG devs Baher_H

### 🔍 View Users & Groups
cat /etc/passwd
cat /etc/group

---

## 📁 Permissions
### 🧾 Check File Permissions
ls -l file.txt
# Example output:
# -rw-r--r-- 1 Baher_H devs 123 Mar 24 10:00 file.txt
- r = read = 4
- w = write = 2
- x = execute = 1

### 🔧 Change Ownership
sudo chown Baher_H:devs file.txt

### 🔧 Change Permissions
chmod 755 script.sh    # rwxr-xr-x
chmod 644 file.txt     # rw-r--r--



