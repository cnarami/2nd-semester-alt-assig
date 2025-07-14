## 2nd-semester-alt-assig

*Project Title:** *The Future of Community-Based Legal Access*

A static web landing page deployed using Ubuntu, Nginx, and AWS EC2 to demonstrate infrastructure provisioning, basic web server configuration, and frontend development using HTML and CSS.

---

## 🌍 Public Access

- **Public IP:** http://your-ec2-public-ip
- **Custom Domain:** (Optional) e.g. http://christian.osinachi.site

---

## 🛠️ Project Overview

This project showcases how cloud infrastructure can be used to deliver accessible digital content. The website explores how legal services can be extended to underserved communities through technology and community-driven support.

The project was built with semantic HTML and responsive CSS, hosted on an AWS EC2 server, and served using Nginx.

---

## 🗃️ Project Structure

ALT-EXAM/
├── index.html # Main landing page
├── css/
│ └── style.css # Styling for the page
├── screenshot.png # Preview of deployed site (optional)
└── README.md # Documentation

yaml
Copy
Edit

---

## 👨‍💻 Technologies Used

- HTML5
- CSS3 (responsive layout)
- Linux (Ubuntu 22.04)
- AWS EC2 (Virtual Server)
- Nginx (Web Server)
- Git & GitHub (Version Control)

---

## 🚀 Step-by-Step Deployment Workflow

### 1️⃣ Provision an EC2 Server on AWS

- Launched a **t2.micro** instance with **Ubuntu 22.04 LTS**
- Created and downloaded a new SSH key pair (`.pem`)
- Opened the following ports in the security group:
  - `22` (SSH)
  - `80` (HTTP)
  - `443` (HTTPS - optional)

---

### 2️⃣ Connect to EC2 via SSH

```bash
chmod 400 christian-key.pem
ssh -i "christian-key.pem" ubuntu@your-ec2-public-ip
3️⃣ Update Server and Install Nginx
bash
Copy
Edit
sudo apt update && sudo apt upgrade -y
sudo apt install nginx -y
sudo ufw allow 'Nginx Full'
Visit your public IP:
http://your-ec2-public-ip
✅ You should see the Nginx welcome page.

4️⃣ Upload Your Project Files
Option A: Use Git

bash
Copy
Edit
sudo apt install git -y
git clone https://github.com/ChristianNarami/ALT-EXAM.git
sudo cp -r ALT-EXAM/* /var/www/html/
sudo rm /var/www/html/index.nginx-debian.html
Option B: Use SCP

bash
Copy
Edit
scp -i christian-key.pem -r * ubuntu@your-ec2-public-ip:/tmp/
ssh ubuntu@your-ec2-public-ip
sudo mv /tmp/index.html /tmp/css /var/www/html/
5️⃣ Restart Nginx to Serve the Site
bash
Copy
Edit
sudo systemctl restart nginx
Now visiting http://your-ec2-public-ip will show your custom site.

6️⃣ (Optional) Add HTTPS with Certbot
If using a custom domain:

bash
Copy
Edit
sudo apt install certbot python3-certbot-nginx -y
sudo certbot --nginx -d yourdomain.com
sudo systemctl enable certbot.timer


