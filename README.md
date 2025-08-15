# 🎓 College Management System

A **full-stack, role-based** College Management System built using **Spring Boot (Backend)** and **ReactJS (Frontend)**.  
The system manages students, faculty, courses, subjects, attendance, exams, and results with **JWT authentication** and **role-based authorization**.

---

## 📌 Features
- **Authentication & Authorization** (JWT, Spring Security)
- **Role-Based Access Control**
  - **Admin**: Manage all modules
  - **Faculty**: Manage attendance, results, and timetable
  - **Student**: View personal info, attendance, results
- Student Management
- Faculty Management
- Department Management
- Course & Subject Management
- Attendance Tracking
- Exam Scheduling
- Result Management
- Timetable Scheduling
- API Documentation with Swagger

---

## 🛠️ Technology Stack

### Backend
- Spring Boot (REST API)
- Spring Security (JWT)
- Spring Data JPA + Hibernate
- MySQL / PostgreSQL
- Lombok
- Jakarta Bean Validation
- Swagger / SpringDoc

### Frontend
- ReactJS
- React Router
- Redux Toolkit
- Axios
- Material-UI / Ant Design
- Formik + Yup

### Tools
- Maven
- npm / yarn
- Git & GitHub
- Postman
- Docker (optional)
- IntelliJ IDEA / VS Code

---

## 📂 Project Structure

### Backend Packages

com.college.management
│── auth # Authentication & JWT
│── student # Student CRUD
│── faculty # Faculty CRUD
│── department # Department CRUD
│── course # Course CRUD
│── subject # Subject CRUD
│── attendance # Attendance management
│── exam # Exam scheduling
│── result # Result management
│── timetable # Timetable management




### Frontend Structure

src/
│── api/ # Axios instances
│── components/ # Reusable UI components
│── pages/ # All pages (Admin, Faculty, Student)
│── features/ # Redux slices
│── hooks/ # Custom hooks
│── utils/ # Helper functions


---

## 🗄️ Database Design

### Entities
- **User** (id, username, password, role)
- **Student** (id, name, roll_no, email, department_id, year, dob)
- **Faculty** (id, name, email, department_id, specialization)
- **Department** (id, name, head_id)
- **Course** (id, name, credits, department_id)
- **Subject** (id, name, course_id, faculty_id)
- **Attendance** (id, student_id, subject_id, date, status)
- **Exam** (id, subject_id, date, type)
- **Result** (id, student_id, subject_id, marks, grade)

### Relationships
- One Department → Many Students, Many Faculty, Many Courses
- One Course → Many Subjects
- One Subject → Many Attendance & Many Exams
- One Exam → Many Results

---

## 🔑 Authentication
- **JWT (JSON Web Token)** used for secure login sessions.
- Passwords hashed using **BCryptPasswordEncoder**.
- Role-based access:
  - `ADMIN`: Full access
  - `FACULTY`: Limited to assigned subjects & students
  - `STUDENT`: Read-only for personal records

---

## 🚀 Installation & Setup

### Backend
```bash
# Navigate to backend folder
cd backend

# Build project
mvn clean install

# Run application
mvn spring-boot:run





# Navigate to frontend folder
cd frontend

# Install dependencies
npm install

# Run application
npm start






🔗 API Documentation

Swagger UI will be available at:

http://localhost:8080/swagger-ui.html




🧪 Testing

Backend: JUnit + Mockito

Frontend: React Testing Library + Jest

Manual API testing: Postman

🌍 Deployment

Backend: Deploy JAR to AWS EC2 / Railway / Render

Frontend: Deploy build to Netlify / Vercel / AWS S3

Use environment variables for DB credentials and JWT secrets.

📅 Roadmap

Backend Setup ✅

Authentication & Authorization ✅

CRUD APIs for all modules ✅

Frontend Pages & Integration ✅

Role-based Routing ✅

Testing ✅

Deployment 🚀





📜 License

This project is licensed under the MIT License.




