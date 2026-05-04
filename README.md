# 🚀 Dockerized Django Notes Application

A production-style **3-tier web application** built using Django, MySQL, and Nginx, fully containerized with Docker and orchestrated using Docker Compose.

---

## 📌 Architecture Overview

```
Client → Nginx (Reverse Proxy)
        ↓
     Django (Gunicorn Server)
        ↓
      MySQL (Database)
```

---

## 🛠️ Tech Stack

* **Backend:** Django (Python)
* **Web Server:** Nginx
* **Database:** MySQL
* **Containerization:** Docker
* **Orchestration:** Docker Compose

---

## ⚙️ Key Features

* Multi-container application using Docker Compose
* Nginx configured as reverse proxy
* Django served with Gunicorn (production-ready)
* MySQL with persistent storage using volumes
* Health checks for container monitoring
* Isolated networking between services

---

## 📂 Project Structure

```
.
├── Dockerfile
├── docker-compose.yml
├── nginx/
│   └── nginx.conf
├── backend/
│   ├── manage.py
│   ├── notesapp/
│   └── requirements.txt
├── .env
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### 1️⃣ Clone the repository

```
git clone https://github.com/your-username/django-docker-nginx-mysql-app.git
cd django-docker-nginx-mysql-app
```

---

### 2️⃣ Run the application

```
docker compose up --build
```

---

### 3️⃣ Access the application

* 🌐 Main App: http://localhost

---

## 🧠 How It Works

* Nginx listens on port **80** and routes traffic to Django
* Django runs on **Gunicorn (port 8000)**
* Django connects to MySQL using Docker service name (`db`)
* Docker Compose manages networking and dependencies

---

## 📸 Screenshots



* Docker containers running (`docker ps`)
<img width="1147" height="244" alt="Screenshot 2026-05-04 145106" src="https://github.com/user-attachments/assets/cc0273d8-589b-4c09-8c19-9c1798df17a9" />

* Application UI
<img width="691" height="817" alt="Screenshot 2026-05-04 145331" src="https://github.com/user-attachments/assets/22775f92-90f9-4c37-925a-0797d5f57818" />

---

## ⚠️ Challenges & Learnings

* Faced database connection issues due to container startup timing
* Understood that `depends_on` does not ensure service readiness
* Learned real-world debugging of container networking and health checks

---

## 📈 Future Improvements

* Static & media file handling via Nginx
* CI/CD pipeline using GitHub Actions or Jenkins
* Deployment using Kubernetes
* Add authentication & API endpoints

---

## 🧾 Resume Highlight

> Deployed a containerized Django application using Docker Compose with Nginx as reverse proxy and MySQL as database. Implemented multi-container orchestration, service networking, and health checks.

## 👨‍💻 Author

**Your Name**
GitHub: https://github.com/shaktisingh647/django-docker-nginx-mysql-app

---

## ⭐ If you like this project

Give it a ⭐ on GitHub!
