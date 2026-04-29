# 👨‍💼 Employee Management System (EMS)

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-green)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey)
![Status](https://img.shields.io/badge/Status-Active-success)

---

## 📌 Overview

The **Employee Management System (EMS)** is a web-based application developed using Flask that helps organizations efficiently manage employees, supervisors, leave requests, and shift schedules.

This system supports **role-based access (Employee, Supervisor, HR)** and automates key operations like leave approval, email notifications, and shift rotation.

> 💡 Designed to streamline HR processes and improve workforce management.

---

## ✨ Key Features

### 🔐 Authentication & Security
- User registration and login  
- Role-based access control (Employee / Supervisor / HR)  
- OTP-based password reset via email  

---

### 👨‍💼 Employee Module
- Apply for leave  
- View leave history  
- Track approved leaves in calendar  
- View personal details  

---

### 🧑‍✈️ Supervisor Module
- Approve / reject leave requests  
- View team members  
- Monitor team leave status  
- Automatic email notification to employees  

---

### 🏢 HR Module
- Add / delete employees  
- Add / delete supervisors  
- View employee & supervisor data  
- Monitor overall workforce  

---

### 📅 Leave Management
- Leave request submission  
- Status tracking (Pending / Approved / Rejected)  
- Email alerts for approvals  

---

### 🔄 Shift Management
- Automated weekly shift rotation  
- View shift schedules  
- Supervisor-specific shift view  

---

### 📧 Email Integration
- OTP verification  
- Leave approval notifications  
- Uses SMTP (Gmail)  

---

## 🧠 System Workflow

flowchart TD
    A[User Login] --> B{Role}
    B -->|Employee| C[Apply Leave]
    B -->|Supervisor| D[Approve/Reject Leave]
    B -->|HR| E[Manage Employees]

    C --> F[Store in Database]



---
## 🛠️ Tech Stack
🔹 Backend
Python 3.8+
Flask
🔹 Database
SQLite (test.db)
🔹 Frontend
HTML
CSS
JavaScript
Jinja2 Templates
🔹 Other Libraries
smtplib (Email sending)
sqlite3
datetime

---
##📂 Project Structure
Employee-Management-System/
├── app.py                 # Main Flask application
├── test.db                # SQLite database
├── templates/             # HTML templates
│   ├── index.html
│   ├── emp.html
│   ├── supervisor.html
│   ├── hr.html
│   ├── leaverequest.html
│   └── ...
├── static/                # CSS, JS, images
├── README.md

---
⚙️ Installation & Setup
✅ Prerequisites
Python 3.8+
pip
Git

---
##🎯 Future Enhancements
🔐 Strong password hashing (bcrypt)
☁️ Cloud database (MySQL / PostgreSQL)
📱 Mobile responsive UI
📊 Advanced analytics dashboard
🔔 Real-time notifications

---
##💡 Use Cases
🏢 Corporate employee management
🏫 Academic staff management
🏭 Workforce tracking systems

---
##⚠️ Security Note
Do NOT expose email credentials in code
Use environment variables for sensitive data
    D --> G[Update Status]
    G --> H[Send Email Notification]
    E --> F
