# System Architecture – Dayflow HRMS

Dayflow follows a three-tier web application architecture designed for security, scalability, and clear role separation.

## 1. Presentation Layer (Frontend)
This is the user interface of the system accessed through a web browser.

It provides:
- Login and Registration screens
- Employee Dashboard
- HR/Admin Dashboard
- Attendance, Leave, and Payroll views

Employees and HR/Admin see different interfaces based on their role after login.

Technologies:
HTML, CSS, JavaScript (or React)

---

## 2. Application Layer (Backend)
This layer contains the core business logic of the system.

It handles:
- User authentication and authorization
- Attendance check-in / check-out
- Leave request submission and approval
- Salary and payroll data processing
- Role-based data access

The backend exposes APIs that the frontend uses to send and receive data.

Technologies:
Node.js / Flask

---

## 3. Data Layer (Database)
This layer stores all system data securely.

It includes:
- User accounts (Employee & HR)
- Attendance records
- Leave requests
- Salary and payroll information

Each record is linked to a specific employee and protected using access control rules.

Technologies:
MongoDB / MySQL

---

## 4. Role-Based Access Control
The system uses role-based access to control what users can do.

Employee:
- View own profile
- Mark attendance
- Apply for leave
- View salary

HR/Admin:
- View all employees
- Approve or reject leave
- Monitor attendance
- Manage payroll

This ensures data security and prevents unauthorized access.
