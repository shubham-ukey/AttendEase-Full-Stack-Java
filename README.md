# EduTrack Pro — Student Attendance Management System

A full-stack web application for managing student attendance, viewing attendance records, and exporting attendance data in CSV and XML formats.

## 🚀 Features

- Student attendance management
- Faculty- and subject-based attendance records
- View and filter attendance records
- RESTful API integration
- Export attendance records to CSV
- Export attendance records to XML
- MySQL database integration
- React-based user interface

## 🛠️ Tech Stack

**Frontend**
- React.js
- Vite
- JavaScript
- Axios
- Tailwind CSS (if configured in the project)

**Backend**
- Java
- Spring Boot
- Spring Web
- Spring Data JPA / Hibernate

**Database**
- MySQL

## 📁 Main Modules

- Admin Dashboard
- Attendance Management
- View Attendance
- Faculty and Subject Records
- CSV/XML Attendance Export

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Configure MySQL

Create a database in MySQL:

```sql
CREATE DATABASE edutrack_db;
```

Configure the database URL, username, and password in the backend's `application.properties` file.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/edutrack_db
spring.datasource.username=YOUR_MYSQL_USERNAME
spring.datasource.password=YOUR_MYSQL_PASSWORD
```

Use the database name and settings required by your existing project.

### 3. Run the backend

Open the Spring Boot project in your IDE and run the main application class.

Local backend URL:

`http://localhost:8091`

### 4. Run the frontend

Open a terminal in the React frontend directory:

```bash
npm install
npm run dev
```

Local frontend URL:

`http://localhost:5173`

If your frontend uses a `VITE_API_URL` environment variable, configure it in `.env`:

```env
VITE_API_URL=http://localhost:8091
```

The variable name must match the one used in your actual frontend code.

## 🔗 Attendance API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/attendance/get-all-attendance-records` | Get attendance records |
| GET | `/attendance/get-attendance-by-faculty/{facultyUsername}` | Get records by faculty |
| GET | `/attendance/get-attendance-by-date-subjet/{date}/{subjectId}` | Get records by date and subject |
| GET | `/attendance/get-attendance/{faculty}/{subjectId}/{date}` | Get filtered records |
| POST | `/attendance/take-attendance` | Submit attendance |
| GET | `/attendance/export/csv` | Export attendance to CSV |
| GET | `/attendance/export/xml` | Export attendance to XML |

### Export examples

Export all records selected by the backend:

```text
http://localhost:8091/attendance/export/csv
http://localhost:8091/attendance/export/xml
```

Export using filters:

```text
http://localhost:8091/attendance/export/csv?facultyUsername=Raj&subjectId=1&date=2026-10-21
```

```text
http://localhost:8091/attendance/export/xml?facultyUsername=Raj&subjectId=1&date=2026-10-21
```

## 🧪 Testing

1. Start MySQL.
2. Start the Spring Boot backend.
3. Start the React frontend.
4. Open the Admin Dashboard or View Attendance page.
5. Test attendance retrieval and CSV/XML downloads.
6. Verify that exported data matches the records stored in the database.

## 👨‍💻 Author

**Shubham Ukey**

Aspiring Full Stack Java Developer

**Technologies:** Java | Spring Boot | React.js | REST APIs | MySQL
