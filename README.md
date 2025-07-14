## 2nd-semester-alt-assig

*Project Title:** *The Future of Community-Based Legal Access*

A static web landing page deployed using Ubuntu, Nginx, and AWS EC2 to demonstrate infrastructure provisioning, basic web server configuration, and frontend development using HTML and CSS.

---


## 🌍 Public Access

- **Public IP:** http://3.94.57.49 
- **(Optional)**  workfgs.crabdance.com

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

- Launch **Ubuntu 22.04** on a `t2.micro` instance
- Create a new SSH key pair 
- Set inbound rules in the security group to allow:
  - Port `22` (SSH)
  - Port `80` (HTTP)
  - Port `443` (HTTPS - optional)

---

### 2️⃣ Connect to EC2 via SSH

```bash
chmod 400 -key.pem
ssh -i "key.pem" ubuntu@your-ec2-public-ip

--



