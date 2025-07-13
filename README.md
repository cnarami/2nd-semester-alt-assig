## 2nd-semester-alt-assig
This project demonstrates the full setup of a cloud-hosted dynamic landing page using AWS EC2, Node.js, and Nginx, with professional deployment practices including reverse proxy configuration and security hardening steps.

## 💡 Project Title
**The Future of Community-Based Legal Access**
## 🎯 Key Goals

- ✅ Deploy a full-stack production environment using **AWS EC2**
- ✅ Host and serve a **static web page using Nginx**
- ✅ Create a modern, responsive **HTML/CSS landing page**
- ✅ Configure firewall and web access via **UFW and security groups**
- ✅  Add **SSL via Let’s Encrypt** for HTTPS

## 🧰 Technologies Used

- **Frontend**: HTML5, CSS3
- **Cloud Platform**: AWS EC2
- **Web Server**: Nginx
- **OS**: Ubuntu 22.04 LTS
- **Tools**: Git, SCP, UFW, SSH, Certbot (optional)

---

## ⚙️ Detailed Deployment Steps

### 1️⃣ Launch AWS EC2 Instance

- AMI: Ubuntu Server 22.04 LTS (t2.micro)
- Configure security group:
  - Port 22 (SSH)
  - Port 80 (HTTP)
  - Port 443 (HTTPS – optional)
- Generate and download your `.pem` SSH key

### 2️⃣ Connect to EC2 via SSH

```bash
chmod 400 your-key.pem
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip

### 3️⃣ Install and Configure Nginx

```bash
sudo apt update && sudo apt install nginx -y
sudo ufw allow 'Nginx Full'
sudo systemctl enable nginx



