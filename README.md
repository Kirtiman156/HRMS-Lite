# HRMS Lite

A lightweight Human Resource Management System for managing employees and tracking attendance.

![HRMS Lite](https://img.shields.io/badge/HRMS-Lite-667eea)
![Python](https://img.shields.io/badge/Python-3.9+-blue)
![React](https://img.shields.io/badge/React-18+-61dafb)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-orange)

## 🌐 Live Demo

- **Frontend**: [Your Vercel URL]
- **Backend API**: [Your Render URL]
- **API Docs**: [Your Render URL]/docs

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
| Database | MySQL |
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
- MySQL 8.0+

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/hrms-lite.git
cd hrms-lite
```

### 2. Setup MySQL Database
```sql
CREATE DATABASE hrms_lite;
```

### 3. Backend Setup
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

# Configure environment
# Edit .env file with your MySQL credentials
# DATABASE_URL=mysql+pymysql://username:password@localhost:3306/hrms_lite

# Run the server
uvicorn main:app --reload
```
Backend will be running at: http://localhost:8000

API Docs available at: http://localhost:8000/docs

### 4. Frontend Setup
```bash
cd frontend

# Install dependencies
npm install

# Configure environment
# Edit .env file if backend is on different port
# VITE_API_URL=http://localhost:8000

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

## 🚢 Deployment

### Backend (Render)
1. Create new Web Service on Render
2. Connect GitHub repository
3. Set build command: `pip install -r requirements.txt`
4. Set start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`
5. Add environment variable: `DATABASE_URL` (MySQL connection string)

### Frontend (Vercel)
1. Import project from GitHub
2. Set framework preset to Vite
3. Add environment variable: `VITE_API_URL` (Render backend URL)
4. Deploy

## ⚠️ Assumptions & Limitations

1. **Single Admin User**: No authentication implemented (as per requirements)
2. **No Leave/Payroll**: Focus on employee and attendance management only
3. **MySQL Required**: Application requires MySQL database
4. **Date Format**: Attendance dates are in YYYY-MM-DD format

## 📝 Future Enhancements

- [ ] Employee profile editing
- [ ] Bulk attendance marking
- [ ] Export attendance reports (CSV/PDF)
- [ ] Employee search and filters
- [ ] Authentication system

## 👤 Author

Built for Ethara AI Technical Assessment

---

Made with ❤️ using React + FastAPI + MySQL
