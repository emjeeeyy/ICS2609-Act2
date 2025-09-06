# Lab CRUD API

A simple CRUD (Create, Read, Update, Delete) API built with **Node.js**, **XAMPP**, **VSCode**, **Postman** and **MySQL**.  
This project manages **students** and **courses** with RESTful endpoints.

Install dependencies
npm install

Make a .env file (use .env.example as a guide)

DB_HOST=localhost
DB_USER=root
DB_PASS=your_password
DB_NAME=lab_crud

Create the database tables
CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  course VARCHAR(100),
  year_level INT
);

CREATE TABLE courses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  code VARCHAR(50) UNIQUE NOT NULL,
  title VARCHAR(255) NOT NULL,
  units INT,
  created_at VARCHAR(50)
);

Run the server(git bash)
npm run dev
or
node server.js

How to Use
Base URL:
http://localhost:3000/api

Student Endpoints
GET /students → get all students
GET /students/:id → get one student
POST /students → add new student
PUT /students/:id → update student
DELETE /students/:id → delete student

Course Endpoints
GET /courses → get all courses
GET /courses/:id → get one course
POST /courses → add new course
PUT /courses/:id → update course
DELETE /courses/:id → delete course

Project Files
lab-crud-api/
├── config/db.js
├── controllers/
│   ├── studentController.js
│   └── courseController.js
├── routes/
│   ├── studentRoutes.js
│   └── courseRoutes.js
├── server.js
├── .env.example
└── README.md
