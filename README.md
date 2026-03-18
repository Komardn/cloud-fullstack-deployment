# 🚀 Cloud Full-Stack Deployment – Portfolio Application

## 📌 Project Overview

Project ini merupakan implementasi deployment aplikasi portfolio berbasis **React (Create React App)** ke lingkungan cloud menggunakan **Virtual Private Server (Ubuntu)**.

Fokus utama project adalah penerapan praktik **Cloud Engineering dan DevOps**, meliputi automated CI/CD deployment, server process management, serta persiapan monitoring dan scaling.

Aplikasi diambil dari template open-source dan dimodifikasi sebagai bagian dari capstone project cloud deployment.

---

## 🏗 System Architecture

User → Internet → Static React App (serve) → PM2 Process Manager → VPS Ubuntu

---

## ⚙️ CI/CD Pipeline

Pipeline otomatis dibuat menggunakan **GitHub Actions**.

Workflow pipeline:

1. Trigger saat push ke branch `main`
2. GitHub Actions melakukan SSH ke VPS
3. Pull source code terbaru
4. Install dependency
5. Build aplikasi
6. Restart aplikasi menggunakan PM2

Pipeline ini memungkinkan **auto-deployment tanpa perlu login manual ke server.**

---

## ☁️ Cloud Deployment

Aplikasi dideploy ke **Virtual Private Server** dengan spesifikasi:

- OS: Ubuntu 20.04
- CPU: 1 vCore
- RAM: 1 GB
- Storage: 25 GB

Application URL:

👉 http://141.11.25.86:3000

Deployment stack:

- NodeJS runtime
- Static build serving menggunakan `serve`
- PM2 sebagai process manager

---

## 🔄 Process Management

Aplikasi dijalankan menggunakan PM2:

- menjaga aplikasi tetap berjalan
- memungkinkan restart otomatis
- mendukung scaling horizontal (cluster mode)

---

## 🚀 Scaling Strategy

Scaling manual dapat dilakukan dengan:

- menjalankan PM2 cluster mode
- upgrade resource VPS

---

## 🔐 Security (Planned Improvement)

Beberapa improvement yang dapat diterapkan:

- firewall UFW
- SSH key authentication
- reverse proxy (Nginx)
- HTTPS termination

---

## 📈 Monitoring (Planned)

Monitoring server resource dapat dilakukan menggunakan:

- Netdata dashboard
- atau Grafana stack

---

## 📚 Run Locally

```bash
npm install
npm run build
npx serve -s build
```

---

## 🙏 Credits

Original template:

https://github.com/codebucks27/wibe-studio

Digunakan sebagai basis implementasi cloud deployment dan automation pipeline.
