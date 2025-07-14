## 2nd-semester-alt-assig

*Project Title:** *The Future of Community-Based Legal Access*

A static web landing page deployed using Ubuntu, Nginx, and AWS EC2 to demonstrate infrastructure provisioning, basic web server configuration, and frontend development using HTML and CSS.

---

## 🌍 Public Access

- **Public IP:** http://your-ec2-public-ip
- **Custom Domain:**

---

## 🛠️ Project Overview

This project showcases how cloud infrastructure can be used to deliver accessible digital content. The website explores how legal services can be extended to underserved communities through technology and community-driven support.

The project was built with semantic HTML and responsive CSS, hosted on an AWS EC2 server, and served using Nginx.

---
OPY THIS INTO README.md:
markdown
Copy
Edit
# 🌐 AltSchool Cloud Engineering Exam Project 

**Project Title:** *The Future of Community-Based Legal Access*

A responsive, cloud-hosted landing page that showcases a vision for expanding legal support through localized technology. This project demonstrates cloud engineering fundamentals: provisioning an Ubuntu server, configuring a web server (Nginx), and deploying static web content.

---

## 🌍 Public Access

- **Public IP:** http://your-ec2-public-ip  
- **(Optional)** Custom Domain: http://christian.yourdomain.com

---

## 🛠️ Project Overview

This project delivers a static HTML/CSS-based landing page hosted on an EC2 server. It emphasizes how grassroots legal assistance — supported by accessible cloud infrastructure — can close the justice gap for underserved communities.

Built with semantic HTML and responsive CSS, the website is deployed via Nginx on an Ubuntu server hosted by AWS EC2.

---

## 📁 Project Structure

ALT-EXAM/
├── index.html # Main landing page content
├── css/
│ └── style.css # Custom styling
├── screenshot.png # (Optional) Preview of deployed site
└── README.md # Project documentation

---

## 👨‍💻 Tech Stack

- HTML5 & CSS3
- Ubuntu 22.04 (Linux)
- Nginx Web Server
- AWS EC2 (t2.micro instance)
- Git & GitHub

---

## 🚀 Step-by-Step Deployment Workflow

### 1️⃣ Provision EC2 Instance

- Launch **Ubuntu 22.04** on a `t2.micro` instance (Free Tier).
- Create a new SSH key pair (`christian-key.pem`).
- Set inbound rules in the security group to allow:
  - Port `22` (SSH)
  - Port `80` (HTTP)
  - Port `443` (HTTPS - optional)

---

### 2️⃣ Connect to EC2 via SSH

```bash
chmod 400 christian-key.pem
ssh -i "christian-key.pem" ubuntu@your-ec2-public-ip

## 3️⃣ Update Server and Install Nginx

sudo apt update && sudo apt upgrade -y
sudo apt install nginx -y
sudo ufw allow 'Nginx Full'
✅ Visit: http://your-ec2-public-ip to confirm the Nginx welcome page appears.

## 4️⃣ Upload Your Project Files
Option A — Using Git
sudo apt install git -y
git clone https://github.com/ChristianNarami/ALT-EXAM.git
sudo cp -r ALT-EXAM/* /var/www/html/
sudo rm /var/www/html/index.nginx-debian.html
Option B — Using SCP from your local machine

scp -i christian-key.pem -r * ubuntu@your-ec2-public-ip:/tmp/
ssh ubuntu@your-ec2-public-ip
sudo mv /tmp/index.html /tmp/css /var/www/html/
### 5️⃣ Restart Nginx
sudo systemctl restart nginx
✅ Now visit: http://your-ec2-public-ip
You should see your deployed site!

### 6️⃣ (Optional) Add HTTPS with Certbot
If you have a custom domain connected via Route53 or other DNS provider:


sudo apt install certbot python3-certbot-nginx -y
sudo certbot --nginx -d yourdomain.com
sudo systemctl enable certbot.timer
📸 Screenshot
Replace this with your screenshot after deployment


![Landing Page]
✅ Project Summary
🚀 Built a clean and responsive static web landing page

⚙️ Provisioned and secured an Ubuntu cloud server (EC2)

🌐 Deployed using Nginx as a production-grade web server

📡  Set up HTTPS with Let’s Encrypt & Certbot

🧠 Demonstrated proficiency in Linux, Git, web hosting, and infrastructure setup



