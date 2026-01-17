# 📔 DayBook – Full Stack MERN Application with DevOps & DevSecOps Practices

## 🌐 Project Overview

**DayBook** is a secure and user-friendly **personal journaling web application** built using the  
**MERN stack (MongoDB, Express, React, Node.js)**.

The application allows users to:
- Securely register and log in
- Create, read, update, delete, and search personal journal entries
- Keep all journal data private using authentication and authorization

This project is used to **understand the complete full-stack flow** of a modern web application and to make it **production-ready** by applying **DevOps and DevSecOps best practices**.

---

## 🧱 Full Stack Architecture

### 🖥️ Frontend (React)
- Built using **React.js**
- Styled with **TailwindCSS & DaisyUI**
- Component-based UI for:
  - Authentication (Login / Signup)
  - Journal entry management (Add / Edit / Delete / Search)
- **Redux Toolkit & RTK Query** for:
  - Global state management
  - API communication and caching
- Fully responsive design

---

### ⚙️ Backend (Node.js & Express)
- RESTful APIs built using **Express.js**
- Follows **MVC architecture**
- Secure authentication using:
  - **JWT tokens**
  - Stored in **HTTP-only cookies** for enhanced security
- Middleware-based route protection
- Centralized error handling and validation

---

### 🗄️ Database (MongoDB)
- MongoDB with **Mongoose ODM**
- Stores:
  - User credentials (hashed passwords)
  - Journal entries linked to authenticated users
- Ensures complete data isolation per user

---

## 🚀 DevOps Practices Implemented

- **Containerization**
  - Dockerized frontend and backend services
  - Multi-stage Docker builds for optimized images

- **CI/CD Pipelines**
  - Automated build, test, scan, and deployment pipelines
  - Tools: **Jenkins / GitHub Actions / GitLab CI**

- **Orchestration**
  - Kubernetes (K8s) for container orchestration
  - Rolling deployments with zero downtime

- **Infrastructure as Code (IaC)**
  - Infrastructure provisioning using **Terraform**

- **Configuration Management**
  - Automated configuration using **Ansible**

- **Monitoring & Observability**
  - Metrics collection using **Prometheus**
  - Dashboards and alerts with **Grafana**

- **Cloud Deployment**
  - Deployed on **AWS Free Tier / Render**
  - Docker image–based deployments

---

## 🛡️ DevSecOps Practices

- Static code analysis using **SonarQube & ESLint**
- Dependency vulnerability scanning with **npm audit & Trivy**
- Docker image security scanning using **Trivy**
- Secure secrets management using:
  - `.env` files
  - Kubernetes Secrets
  - Cloud secret managers
- Security gates in CI/CD pipelines to block high-severity issues
- Security monitoring integrated with observability stack

---

## 🛠️ Tech Stack

**Frontend:**  
React.js, TailwindCSS, DaisyUI, Redux Toolkit, RTK Query

**Backend:**  
Node.js, Express.js, MongoDB, Mongoose, JWT

**DevOps / DevSecOps:**  
Docker, Kubernetes, Jenkins, GitHub Actions, GitLab CI  
Terraform, Ansible  
Prometheus, Grafana  
SonarQube, Trivy

---

## ▶️ How to Start the Project Locally

### Prerequisites
- Git
- Node.js (v18+ recommended)
- MongoDB (local or cloud)
- Docker (optional but recommended)

---

### 🔹 Backend Setup

```bash
git clone https://github.com/thenileshnishad/daybook.git
cd daybook/backend
npm install
Create a .env file in the backend directory:

env
Copy code
PORT=3000
MONGO_URI=mongodb://localhost:27017/daybook
JWT_SECRET=your_secret_key
FRONTEND_URL=http://localhost:5173
Start the backend server:

bash
Copy code
npm run dev
# or
npm start
🔹 Frontend Setup
bash
Copy code
cd ../frontend
npm install
Create a .env file in the frontend directory:

env
Copy code
VITE_BACKEND_URL=http://localhost:3000
Start the frontend:

bash
Copy code
npm run dev
🔹 Access the Application
Frontend → http://localhost:5173

Backend → http://localhost:3000

🎯 Learning Objectives
Understand end-to-end full stack application flow

Build production-grade CI/CD pipelines

Apply DevSecOps principles in real projects

Gain hands-on experience with:

Docker & Kubernetes

Terraform & Ansible

Cloud deployments

Learn real-world system scalability, security, and reliability