# 📔 DayBook – Full Stack MERN Journaling Application

🌐 **Live Demo:**  
👉 http://daybook-mern.vercel.app/

---

## 🧠 Overview

**DayBook** is a secure and user-friendly **personal journaling web application** built using the  
**MERN stack (MongoDB, Express, React, Node.js)**.

The application allows users to safely record their daily thoughts and memories while ensuring
**privacy, simplicity, and a distraction-free experience**.

This project also serves as a **hands-on Full Stack + DevOps learning project**, where the focus is on
understanding real-world application flow, CI/CD pipelines, security scanning, and containerized builds.

---

## ✨ Key Features

- 🔐 Secure user authentication (JWT + HTTP-only cookies)
- 📝 Create, read, update, and delete journal entries
- 🔍 Search entries by title or content
- 👤 User profile and password management
- 🎨 Clean, responsive, and minimal UI
- ⚡ Fast client-side state management with caching

---

## 🏗️ Tech Stack

### Frontend
- React.js
- Redux Toolkit & RTK Query
- TailwindCSS & DaisyUI
- Vite

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication

### DevOps & DevSecOps
- Docker (multi-stage builds)
- GitHub Actions (CI/CD)
- SonarCloud (static code analysis)
- Trivy (filesystem & container vulnerability scanning)

---

## 🧩 Application Architecture

```text
User
 ↓
React Frontend
 ↓
Node.js / Express API
 ↓
MongoDB Database
Authentication Flow
text
Copy code
Login → JWT Generated → Stored in HTTP-only Cookie → Protected Routes
📂 Project Structure
bash
Copy code
daybook/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   └── utils/
│   ├── Dockerfile
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   └── assets/
│   ├── Dockerfile
│   └── package.json
│
├── .github/
│   └── workflows/
│       └── CI-CD.yml
│
└── README.md
🚀 CI/CD Pipeline (GitHub Actions)
The project includes an automated CI/CD pipeline that performs:

✅ Source code checkout

✅ Node.js environment setup

✅ SonarCloud static code analysis

✅ Trivy filesystem vulnerability scanning

✅ Docker image build (frontend & backend)

✅ Trivy container image security scanning

🔒 Security scans are integrated early to follow DevSecOps principles.

🛠️ Local Setup (Development)
Prerequisites
Node.js (v18+)

MongoDB

Git

Docker (optional)

Backend Setup
bash
Copy code
git clone https://github.com/<your-username>/daybook-devops.git
cd daybook/backend
npm install
Create .env file in backend/:

env
Copy code
PORT=3000
MONGO_URI=mongodb://localhost:27017/daybook
JWT_SECRET=your_secret_key
FRONTEND_URL=http://localhost:5173
Start backend server:

bash
Copy code
npm run dev
Frontend Setup
bash
Copy code
cd ../frontend
npm install
Create .env file in frontend/:

env
Copy code
VITE_BACKEND_URL=http://localhost:3000
Start frontend server:

bash
Copy code
npm run dev
🌍 Access URLs
Frontend → http://localhost:5173

Backend → http://localhost:3000

🎯 Learning Outcomes
Built and understood an end-to-end Full Stack MERN application

Implemented secure authentication and authorization

Designed CI/CD pipelines using GitHub Actions

Applied DevSecOps practices with real security tools

Worked with Dockerized builds and automated scans

Learned how production systems enforce quality and security gates

