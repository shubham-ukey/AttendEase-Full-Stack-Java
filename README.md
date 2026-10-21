# AttendEase — Full Stack Student Attendance Management System

**Simplifying Student Attendance Management.**

AttendEase is a full-stack web application designed to manage student attendance records, retrieve attendance information, and export reports in CSV and XML formats. It uses React.js for the frontend, Spring Boot for the backend, and MySQL for database management.

## 🚀 Features

- Manage and view student attendance records
- Retrieve attendance by faculty, subject, and date
- REST API integration between frontend and backend
- Export attendance records to CSV
- Export attendance records to XML
- Download filtered attendance reports
- MySQL database integration
- User-friendly web interface

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| React.js | Frontend development |
| Java | Backend programming |
| Spring Boot | REST API development |
| Spring Data JPA / Hibernate | Database operations |
| MySQL | Relational database |
| Axios | HTTP requests |
| Git & GitHub | Version control |

## 📂 Project Modules

- Admin Dashboard
- Attendance Management
- View Attendance
- Faculty and Subject Records
- CSV/XML Report Export

## ⚙️ Installation and Setup

### Prerequisites

- Java JDK compatible with the project's Spring Boot version
- Node.js and npm
- MySQL Server
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/shubham-ukey/AttendEase-Full-Stack-Java.git
cd AttendEase-Full-Stack-Java
```

### 2. Configure MySQL

Create a database in MySQL:

```sql
CREATE DATABASE edutrack_db;
```

Configure your database connection in the backend's `application.properties` file:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/edutrack_db
spring.datasource.username=YOUR_MYSQL_USERNAME
spring.datasource.password=YOUR_MYSQL_PASSWORD
```

Use the database name and configuration expected by your existing backend. Never commit real database credentials to GitHub.

### 3. Run the Backend

Open the Spring Boot project in Eclipse or IntelliJ IDEA and run the main application class.

The local backend URL is:

```text
http://localhost:8091
```

### 4. Run the Frontend

Open a terminal in the React frontend directory:

```bash
npm install
npm run dev
```

The frontend is expected to run at:

```text
http://localhost:5173
```

If your frontend uses an environment variable for the API base URL, configure it in `.env` according to your `apiService.js` implementation.

## 🔗 Attendance API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/attendance/get-all-attendance-records` | Retrieve all attendance records |
| GET | `/attendance/get-attendance-by-faculty/{facultyUsername}` | Retrieve records by faculty |
| GET | `/attendance/get-attendance-by-date-subjet/{date}/{subjectId}` | Retrieve records by date and subject |
| GET | `/attendance/get-attendance/{faculty}/{subjectId}/{date}` | Retrieve filtered attendance |
| POST | `/attendance/take-attendance` | Submit attendance |
| GET | `/attendance/export/csv` | Export records as CSV |
| GET | `/attendance/export/xml` | Export records as XML |

Confirm the endpoint names and request formats against the current backend controller before integrating external clients.

## 📊 Attendance Report Export

AttendEase supports exporting attendance records in two formats:

- **CSV:** Useful for spreadsheets and tabular reports.
- **XML:** Useful for structured data exchange and integrations.

Optional export filters include faculty username, subject ID, and date, depending on the backend implementation.

Example:

```text
http://localhost:8091/attendance/export/csv
http://localhost:8091/attendance/export/xml
```

## 🧪 Testing

1. Start the MySQL server.
2. Run the Spring Boot backend.
3. Start the React frontend.
4. Open the attendance section.
5. Verify attendance records.
6. Test CSV and XML downloads.
7. Confirm that exported data matches the records stored in the database.

## 🔮 Future Enhancements

- Role-based authentication and authorization
- Attendance analytics and dashboard charts
- Pagination and advanced filtering
- Automated testing
- Cloud deployment

## 👨‍💻 Author

**Shubham Ukey**

Full Stack Java Developer

GitHub: [shubham-ukey](https://github.com/shubham-ukey)

---

*AttendEase — Making Attendance Management Simpler.*
