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

### 👤 Create a User
```bash
sudo useradd -m Baher_H
sudo passwd Baher_H
```
### 👨‍👩‍👧‍👦 Create a Group
```bash
sudo groupadd devs
```
### Add User to Group
```bash
sudo usermod -aG devs Baher_H
```
### 🔍 View Users & Groups
```bash
cat /etc/passwd
cat /etc/group
```
---

## 📁 Permissions
### 🧾 Check File Permissions
```bash
ls -l file.txt

# Example output:
"""
-rw-r--r-- 1 Baher_H devs 123 Mar 24 10:00 file.txt
- r = read = 4
- w = write = 2
- x = execute = 1
"""
```
### 🔧 Change Ownership
```bash
sudo chown Baher_H:devs file.txt
```
### 🔧 Change Permissions
```bash
chmod 755 script.sh    # rwxr-xr-x
chmod 644 file.txt     # rw-r--r--
```


