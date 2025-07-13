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
3️⃣ Install and Configure Nginx
bash
Copy
Edit
sudo apt update && sudo apt install nginx -y
sudo ufw allow 'Nginx Full'
sudo systemctl enable nginx
4️⃣ Upload Files to Server
Option A: Clone from GitHub
bash
Copy
Edit
sudo apt install git -y
git clone https://github.com/ChristianNarami/ALT-EXAM.git
sudo cp -r ALT-EXAM/* /var/www/html/
sudo rm /var/www/html/index.nginx-debian.html
Option B: Upload via SCP
bash
Copy
Edit
scp -i your-key.pem -r * ubuntu@your-ec2-public-ip:/tmp/
ssh ubuntu@your-ec2-public-ip
sudo mv /tmp/index.html /tmp/css /var/www/html/
5️⃣ Restart Nginx
bash
Copy
Edit
sudo systemctl restart nginx
6️⃣ (Optional) Enable HTTPS with Certbot
bash
Copy
Edit
sudo apt install certbot python3-certbot-nginx -y
sudo certbot --nginx -d yourdomain.com
✅ Outcome
This project demonstrates the ability to:

Deploy a static web page to the public internet via cloud infrastructure

Use Nginx to serve content securely and efficiently

Follow best practices in web deployment and system security

Build and document a clean, responsive front-end experience

Explain a deployment workflow in a real-world DevOps context




