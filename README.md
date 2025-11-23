# Online-Fitness-Tracker-Java-Project
Online FitTrack – Full-Stack Fitness Tracking Application

Online FitTrack is a full-stack fitness tracking platform that allows users to log workouts, track fitness progress, join challenges, and manage their profile.
Administrators can manage users, review fitness content, configure system settings, and monitor platform activity.

This project is built using:

Java Spring Boot – Backend (REST API, Authentication, Database)

React + Tailwind CSS – Frontend (UI)

PostgreSQL – Database

Docker Compose – Optional containerized deployment

🚀 Features
User Features

Login & Signup with JWT Authentication

Log workouts (type, duration, intensity, notes)

View list of all logged workouts

Track progress through log history

Join and participate in fitness challenges

Manage personal profile

Admin Features

Manage users (add/update/delete)

Approve or reject fitness content

View platform-wide statistics

Manage system settings

Monitor system activity

🏗️ Tech Stack
Backend

Java 17

Spring Boot (Web, Security, JPA, Validation)

JWT authentication

PostgreSQL

Maven

Frontend

React

React Router

Tailwind CSS

Axios

DevOps

Docker & Docker Compose

REST API

📂 Project Structure
online-fittrack/
├── backend/              # Spring Boot backend
├── frontend/             # React + Vite + Tailwind frontend
├── docker-compose.yml    # Run everything with Docker
└── README.md             # Project documentation

⚙️ How to Run the Project

You can run the project using Docker (recommended) or manually.

🐳 Running with Docker (Easiest)
Requirements

Docker

Docker Compose

Steps
docker-compose up --build

After successful start:

Frontend: http://localhost:3000

Backend API: http://localhost:8080/api/v1

🏃 Running Manually (Without Docker)
Backend

Install Java 17 and Maven

Start PostgreSQL locally

Update DB credentials in:

backend/src/main/resources/application.properties


Run backend:

cd backend
mvn clean package
java -jar target/backend-0.0.1-SNAPSHOT.jar

Frontend
cd frontend
npm install
npm run dev

🔐 Authentication (JWT)

Sign up at:
POST /api/v1/auth/signup

Log in at:
POST /api/v1/auth/login

You will receive a JWT token.
Store it in localStorage.
Every protected request uses:

Authorization: Bearer <token>

📌 API Overview
Auth
Method	Endpoint	Description
POST	/auth/signup	Register
POST	/auth/login	Login & receive JWT
Workouts
Method	Endpoint	Description
GET	/workouts	Get user workouts


POST	/workouts	Log a workout

(More endpoints can be added if required.)
