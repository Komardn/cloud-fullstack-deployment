# 🚀 Cloud Full-Stack Deployment – Wibe Studio Portfolio

## 📌 Project Overview

Project ini merupakan implementasi deployment aplikasi full-stack berbasis **NextJS** ke lingkungan cloud menggunakan **VPS Ubuntu**.

Fokus utama project ini adalah penerapan praktik **DevOps dan Cloud Engineering**, meliputi CI/CD automation, deployment server, monitoring performa, serta konfigurasi keamanan dasar.

Aplikasi yang digunakan merupakan UI portfolio template open-source yang telah dimodifikasi dan dideploy sebagai bagian dari capstone project.

---

## 🏗 System Architecture

User → Internet → Nginx Reverse Proxy → NextJS Application (PM2) → VPS Server

---

## ⚙️ CI/CD Pipeline

Pipeline otomatis dibuat menggunakan **GitHub Actions** dengan tahapan:

1. Checkout source code
2. Install dependency
3. Build aplikasi NextJS
4. Deploy otomatis ke VPS melalui SSH
5. Restart aplikasi menggunakan PM2

Pipeline akan berjalan setiap kali terjadi push ke branch **main**.

---

## ☁️ Cloud Deployment

Aplikasi dideploy ke **Virtual Private Server (Ubuntu)** dengan spesifikasi:

- Hostname: **finalprojectkomar.com**
- IP Address: **141.11.175.86**
- 1 vCPU
- 1 GB RAM
- 25 GB Storage

Aplikasi dapat diakses melalui:

👉 http://141.11.175.86

Deployment menggunakan:

- NodeJS runtime
- PM2 process manager
- Nginx reverse proxy

---

## 📈 Monitoring

Monitoring server dilakukan menggunakan **Netdata dashboard** untuk memantau:

- CPU Usage
- Memory Usage
- Network Traffic
- Disk I/O

Monitoring membantu memastikan performa aplikasi tetap stabil setelah deployment.

---

## 🔐 Security Implementation

Beberapa konfigurasi keamanan yang diterapkan:

- SSH authentication menggunakan key (tanpa password login)
- Firewall aktif menggunakan UFW
- Environment variable tidak di-hardcode dalam source code
- Reverse proxy untuk membatasi direct access ke aplikasi

---

## 🚀 Scaling Strategy (Manual)

Aplikasi dapat di-scale secara manual dengan:

- Menjalankan multiple instance menggunakan PM2 cluster mode
- Upgrade spesifikasi VPS

---

## 📚 How to Run Locally

```
npm install
npm run build
npm run start
```

---

## 🙏 Credits

Original UI Template:
https://github.com/codebucks27/wibe-studio

Template digunakan sebagai dasar implementasi deployment cloud dan praktik DevOps pada project ini.
