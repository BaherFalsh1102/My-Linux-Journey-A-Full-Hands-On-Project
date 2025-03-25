# 🖥️ Managing Services & Daemons in Linux

## ✅ Goal:
Understand how to manage system services using `systemd`, configure a web server (Apache), and secure SSH for remote access.

---

## 🔧 Tools & Commands:
- `systemctl`, `service`
- `journalctl` (logs)
- `nginx` / `apache2`
- `ssh`, `sshd`

---

## 🔄 1️⃣ Managing Services with systemd
### 🔍 Check the Status of a Service
```bash
sudo systemctl status apache2
```
### ▶️ Start / Stop / Restart a Service
```bash
sudo systemctl start apache2
sudo systemctl stop apache2
sudo systemctl restart apache2
```
### 🔄 Enable a Service at Boot
```bash
sudo systemctl enable apache2
```
### 🚫 Disable a Service at Boot
```bash
sudo systemctl disable apache2
```
---
## 🌐 2️⃣ Installing & Configuring a Web Server (Apache)
### 🛠️ Install Apache
```bash
sudo apt update && sudo apt install apache2 -y   # Ubuntu/Debian
```
### 📄 Check Apache Service
```bash
sudo apt update && sudo apt install apache2 -y   # Ubuntu/Debian
```
### 📂 Default Web Directory (Ubuntu Example)
```bash
ls /var/www/html
```
### 📝 Modify Default Web Page
```bash
echo "<h1>Welcome to My Linux Project</h1>"
sudo tee /var/www/html/index.html
```
### 🔥 Allow HTTP Traffic on Firewall
```bash
sudo ufw allow 80/tcp   # Ubuntu
sudo firewall-cmd --reload
```
### 🌍 Test Web Server
```bash
# Open a browser and visit:
http://your-server-ip
```
---
## 🔑 3️⃣ Configuring & Securing SSH
### 📥 Install SSH Server (if not installed)
```bash
sudo apt install openssh-server -y   # Ubuntu
```
### 🔍 Check SSH Service
```bash
sudo systemctl status ssh
```
### 🚀 Connect to Your Server via SSH
```bash
ssh username@your-server-ip
```
### 🔒 Secure SSH (Disable Root Login)
```bash
sudo nano /etc/ssh/sshd_config
```
### 🔄 Restart SSH for Changes to Take Effect
```bash
sudo systemctl restart ssh
```


