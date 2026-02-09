# HRMS Lite

A lightweight Human Resource Management System for managing employees and tracking attendance.

![HRMS Lite](https://img.shields.io/badge/HRMS-Lite-667eea)
![Python](https://img.shields.io/badge/Python-3.9+-blue)
![React](https://img.shields.io/badge/React-18+-61dafb)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-336791)

## 🌐 Live Demo

- **Frontend**: https://kirtiman156.github.io/HRMS-Lite
- **Backend API**: https://hrms-lite-api-08mz.onrender.com
- **API Docs**: https://hrms-lite-api-08mz.onrender.com/docs

## 📋 Features

### Core Features
- ✅ **Employee Management**
  - Add new employees (ID, Name, Email, Department)
  - View all employees in a card grid
  - Delete employees with confirmation

- ✅ **Attendance Tracking**
  - Mark daily attendance (Present/Absent)
  - View attendance history
  - Filter by date range (Bonus)

- ✅ **Dashboard**
  - Employee count overview
  - Today's attendance summary
  - Department breakdown
  - Recent attendance activity

### Technical Features
- RESTful API with proper status codes
- Server-side validation (required fields, email format, duplicates)
- Meaningful error messages
- Loading, empty, and error states in UI
- Responsive design

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React 18 + Vite |
| Backend | FastAPI (Python) |
| Database | PostgreSQL |
| ORM | SQLAlchemy |
| Styling | Vanilla CSS |

## 📁 Project Structure

```
HRMS-Lite/
├── backend/
│   ├── routes/
│   │   ├── employees.py
│   │   ├── attendance.py
│   │   └── dashboard.py
│   ├── main.py
│   ├── models.py
│   ├── schemas.py
│   ├── database.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── index.css
│   ├── index.html
│   └── package.json
│
└── README.md
```

## 🚀 Local Development Setup

### Prerequisites
- Python 3.9+
- Node.js 18+
- PostgreSQL (or SQLite for local testing)

### 1. Clone the Repository
```bash
git clone https://github.com/Kirtiman156/HRMS-Lite.git
cd HRMS-Lite
```

### 2. Backend Setup
```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the server
uvicorn main:app --reload
```
Backend will be running at: http://localhost:8000

API Docs available at: http://localhost:8000/docs

### 3. Frontend Setup
```bash
cd frontend

# Install dependencies
npm install

# Run development server
npm run dev
```
Frontend will be running at: http://localhost:5173

## 📡 API Endpoints

### Employees
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/employees | Get all employees |
| GET | /api/employees/{id} | Get single employee |
| POST | /api/employees | Create new employee |
| DELETE | /api/employees/{id} | Delete employee |

### Attendance
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/attendance | Get all attendance (supports date filters) |
| GET | /api/attendance/employee/{id} | Get employee's attendance |
| POST | /api/attendance | Mark attendance |

### Dashboard
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/dashboard/stats | Get dashboard statistics |

## ⚠️ Notes

1. **Single User Mode**: No authentication (as per requirements)
2. **Focus**: Employee and attendance management only
3. **Date Format**: Attendance dates are in YYYY-MM-DD format

## 👤 Author

Built for Ethara AI Technical Assessment
