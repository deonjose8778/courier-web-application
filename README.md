# Courier App Monorepo

A full-stack courier management platform with real-time shipment tracking, user management, and automated logistics. This repository contains both the backend (FastAPI) and frontend (React) applications.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Folder Structure](#folder-structure)
- [Backend](#backend)
  - [Features](#backend-features)
  - [Setup & Installation](#backend-setup--installation)
  - [Environment Variables](#backend-environment-variables)
  - [Running the Backend](#running-the-backend)
- [Frontend](#frontend)
  - [Features](#frontend-features)
  - [Setup & Installation](#frontend-setup--installation)
  - [Running the Frontend](#running-the-frontend)
- [License](#license)

---

## Project Overview

Courier App is a platform to manage shipments, users, addresses, and payments. It provides real-time tracking, automated logistics, and a modern dashboard for both suppliers and importers/exporters.

---

## Folder Structure

```
Courier_App/
├── backend/   # FastAPI backend (APIs, DB, Auth, Alembic, etc.)
├── frontend/  # React frontend (Vite, Tailwind, Dashboard, etc.)
└── README.md  # Project documentation (this file)
```

---

## Backend

### Backend Features
- FastAPI-based RESTful API
- JWT authentication & user management
- PostgreSQL database (SQLAlchemy ORM)
- Alembic migrations
- Email (SMTP) support for password reset
- Razorpay integration for payments
- Modular structure for shipments, users, addresses, and packages

### Backend Setup & Installation

1. **Navigate to backend folder:**
   ```sh
   cd backend
   ```
2. **Create and activate a virtual environment:**
   ```sh
   python3 -m venv venv
   source venv/bin/activate
   ```
3. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
4. **Configure environment variables:**
   - Copy `.env.example` to `.env` and fill in your database, JWT, SMTP, and Razorpay credentials.

### Backend Environment Variables
- `environment`, `db_user`, `db_pass`, `db_host`, `db_name`, `db_port`
- `secret_key`, `algorithm`, `access_token_expire_minutes`, `refresh_token_expire_days`
- `razorpay_key_id`, `razorpay_key_secret`
- `smtp_from_email`, `smtp_user`, `smtp_password`, `smtp_host`, `smtp_port`
- `APP_HOST`, `FORGET_PASSWORD_URL`

### Running the Backend

```sh
uvicorn main:app --reload
```
- The API will be available at `http://localhost:8000/`

---

## Frontend

### Frontend Features
- React (Vite) SPA with modern UI
- Tailwind CSS for styling
- React Router for navigation
- JWT-based authentication (integrates with backend)
- Dashboard with charts (Recharts)
- Toast notifications (react-toastify)
- Shipment creation, editing, and tracking
- User profile and address management

### Frontend Setup & Installation

1. **Navigate to frontend folder:**
   ```sh
   cd frontend
   ```
2. **Install dependencies:**
   ```sh
   npm install
   ```

### Running the Frontend

```sh
npm run dev
```
- The app will be available at `http://localhost:5173/` (default Vite port)
- Make sure the backend is running at `http://localhost:8000/` (or update the API URL in `src/utils/axiosInstance.jsx`)

---

## License

This project is licensed under the MIT License. 