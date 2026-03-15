# 🚀 Task Board - N-Tier Architecture (Docker + Railway)

## ENGCE301 - Week 7 Cloud Deployment Lab

---

## 👤 Student Information

- **Name:** นายจิรภัทร จันทร์เทพ
- **Student ID:** 66543206023-4

---

# 📌 Project Overview

This project demonstrates deployment of a **Task Board application** using **N-Tier Architecture** with **Docker** and **Cloud Platform (Railway)**.

The system is divided into three main layers:

- **Frontend** – Web interface for managing tasks  
- **Backend API** – REST API built with Node.js and Express  
- **Database** – PostgreSQL for storing task data  

---

# 🏗 System Architecture

Frontend (Browser)
│
▼
Backend API (Node.js / Express)
│
▼
PostgreSQL Database


All services are deployed on **Railway Cloud Platform**.

---

# 🌐 Live Deployment

| Service | URL |
|------|-----|
| Frontend | https://attractive-spirit-production-e8e6.up.railway.app |
| Backend API | https://engce301-week6-ntier-docker-production.up.railway.app |
| API Health Check | https://engce301-week6-ntier-docker-production.up.railway.app/api/health |
| Database | Internal (Railway PostgreSQL) |

---

# ✨ Features

- Create tasks
- Update task status
- Delete tasks
- Task statistics dashboard
- Priority management

---

# 🧰 Technology Stack

### Frontend
- HTML
- CSS
- JavaScript

### Backend
- Node.js
- Express.js
- REST API

### Database
- PostgreSQL

### Deployment
- Docker
- Railway Cloud Platform
- GitHub

---

# 🔗 API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| GET | `/api/tasks` | Get all tasks |
| GET | `/api/tasks/:id` | Get task by ID |
| POST | `/api/tasks` | Create new task |
| PUT | `/api/tasks/:id` | Update task |
| DELETE | `/api/tasks/:id` | Delete task |
| GET | `/api/tasks/stats` | Get task statistics |
| GET | `/api/health` | API health check |


# 🐳 Running Locally with Docker

## Clone repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```
Start services
```
docker compose up -d
```
Access application

Frontend:
http://localhost:8080

Backend API:
http://localhost:3000/api

⚙ Environment Variables
```Example .env
DB_HOST=db
DB_PORT=5432
DB_NAME=taskboard_db
DB_USER=taskboard
DB_PASSWORD=password
NODE_ENV=development
PORT=3000
```


📂 Repository Structure
```
week6-ntier-docker/
│
├── api/                    # Backend API
│   ├── package.json
│   ├── server.js
│   └── src/
│
├── frontend/               # Frontend application
│   ├── index.html
│   ├── css/style.css
│   └── js/app.js
│
├── database/               # Database initialization
│   └── init.sql
│
├── screenshots/            # Deployment screenshots
│   ├── dashboard.png
│   ├── frontend.png
│   ├── api-health.png
│   ├── logs.png
│   └── metrics.png
│
├── docker-compose.yml
├── CLOUD_DEPLOYMENT.md
└── README.md
```

# 📊 สรุปผลลัพธ์การทดลอง

## 🎯 วัตถุประสงค์การทดลอง

- สร้างและพัฒนา **Task Board Application** โดยใช้ **N-Tier Architecture**
- เรียนรู้กระบวนการ **Containerization** ด้วย Docker
- ประสบการณ์การ **Deploy แอปพลิเคชัน** บน **Cloud Platform (Railway)**
- ศึกษาการทำงานของระบบแบบ **Multi-tier** รวมถึง Frontend, Backend, และ Database

## ✅ สิ่งที่ทำสำเร็จ

### 1. การพัฒนา Frontend
- สร้าง Web Interface ด้วย HTML, CSS, JavaScript
- ฟีเจอร์การจัดการ Tasks: สร้าง, อ่าน, อัปเดต, ลบ (CRUD)
- Dashboard สำหรับแสดงสถิติ Tasks
- จัดการ Priority และ Status ของ Tasks

### 2. การพัฒนา Backend API
- พัฒนา REST API ด้วย Node.js และ Express.js
- จัดการ Routing, Controllers, Services, และ Repositories
- Middleware สำหรับ Error Handling
- Database Connection ด้วย PostgreSQL

### 3. การตั้งค่า Database
- ใช้ PostgreSQL เป็นฐานข้อมูล
- สร้าง Schema และ Initial Data ด้วย SQL Script
- จัดการ Database Migrations และ Connections

### 4. Containerization ด้วย Docker
- สร้าง Dockerfile สำหรับแต่ละ Service (API, Frontend, Database, Nginx)
- ตั้งค่า Docker Compose สำหรับ Orchestration
- จัดการ Environment Variables และ Networking

### 5. การ Deploy บน Cloud
- Deploy บน **Railway Cloud Platform**
- ตั้งค่า Environment Variables สำหรับ Production
- จัดการ SSL Certificates และ Domain
- Monitoring และ Logging

## 🔧 ความท้าทายและการแก้ปัญหา

### ความท้าทายที่พบ
- **การตั้งค่า Environment Variables**: ต้องปรับแต่งสำหรับ Development และ Production Environment
- **Database Connection Issues**: แก้ปัญหา Connection Pooling และ Error Handling
- **Nginx Configuration**: ตั้งค่า Reverse Proxy และ Load Balancing
- **Cloud Deployment**: จัดการ Resource Limits และ Scaling บน Railway

### วิธีการแก้ปัญหา
- ศึกษาจาก Documentation ของ Docker และ Railway
- ทดสอบ Local Environment ก่อน Deploy
- ใช้ Health Check Endpoints เพื่อตรวจสอบสถานะ Service
- จัดการ Logs และ Monitoring เพื่อ Debug Issues

## 📈 ผลการทดสอบและการทำงาน

### Local Testing
- **Frontend**: เข้าถึงได้ที่ `http://localhost:8080`
- **Backend API**: ทำงานได้ที่ `http://localhost:3000/api`
- **Database**: PostgreSQL Container ทำงานปกติ
- **Docker Compose**: Services ทำงานร่วมกันได้อย่างสมบูรณ์

### Cloud Deployment
- **Frontend**: https://attractive-spirit-production-e8e6.up.railway.app
- **Backend API**: https://engce301-week6-ntier-docker-production.up.railway.app
- **API Health Check**: https://engce301-week6-ntier-docker-production.up.railway.app/api/health
- **Database**: Railway PostgreSQL (Internal)

### API Endpoints ที่ทดสอบแล้ว
- ✅ GET `/api/tasks` - ดึงข้อมูล Tasks ทั้งหมด
- ✅ GET `/api/tasks/:id` - ดึงข้อมูล Task แบบเจาะจง
- ✅ POST `/api/tasks` - สร้าง Task ใหม่
- ✅ PUT `/api/tasks/:id` - อัปเดต Task
- ✅ DELETE `/api/tasks/:id` - ลบ Task
- ✅ GET `/api/tasks/stats` - สถิติ Tasks
- ✅ GET `/api/health` - Health Check

## 📚 การเรียนรู้และประสบการณ์

### ความรู้ที่ได้รับ
- **N-Tier Architecture**: เข้าใจการแยก Layer ของ Application
- **Docker & Containerization**: ความรู้เรื่อง Container, Images, และ Orchestration
- **Cloud Deployment**: ประสบการณ์ Deploy บน Platform as a Service (PaaS)
- **DevOps Practices**: CI/CD, Monitoring, และ Environment Management
- **Full-Stack Development**: การพัฒนาทั้ง Frontend และ Backend

### ทักษะที่พัฒนา
- การออกแบบและพัฒนา REST API
- การจัดการ Database และ SQL
- การเขียน Dockerfile และ Docker Compose
- การ Deploy และ Maintain Application บน Cloud
- การ Debug และ Troubleshooting ใน Production Environment

## 👨‍🎓 ข้อมูลนักศึกษา

- **ชื่อ-นามสกุล**: นายจิรภัทร จันทร์เทพ
- **รหัสนักศึกษา**: 66543206023-4
- **วิชา**: ENGCE301 - Cloud Computing
- **สัปดาห์ที่**: Week 7 - Cloud Deployment Lab

---

*รายงานนี้จัดทำขึ้นเพื่อแสดงผลการทำงานของโปรเจกต์ Task Board N-Tier Architecture ตามความต้องการของอาจารย์ผู้สอน*
```