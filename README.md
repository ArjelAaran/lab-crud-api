**PROJECT OVERVIEW**

This Lab CRUD API is a functional REST API and is designed to demonstrate how to build and structure a backend API that performs CRUD operations.

This project manages two resources:

- Students
- Courses

This API also has CORS enabled to ensure compatibility with front-end applications.

**SETUP STEPS**

1. Close the repo

	Paste in terminal

git clone https://github.com/your-username/lab-crud-api.git
cd lab-crud-api

2. Install dependencies
	
	Paste in terminal

npm install

3. Set up database

- Create a database in MySQL (lab_crud)
- Create the tables:

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  course VARCHAR(100),
  year_level INT
);

CREATE TABLE courses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  code VARCHAR(20) UNIQUE NOT NULL,
  name VARCHAR(100) NOT NULL,
  description TEXT
);

4. Copy .env.example and RENAME to .env

	Make sure to update database credentials accordingly

**HOW TO RUN**

Go to root terminal and enter:

	npm run dev

Server will run at http://localhost:[PORT]

**LIST OF ENDPOINTS**

HEALTH CHECK

- GET /api/health

STUDENTS

- POST /api/students 

- GET /api/students 

- GET /api/students/:id 

- PUT /api/students/:id 

- DELETE /api/students/:id 

COURSES

- POST /api/courses  

- GET /api/courses  

- GET /api/courses/:id 

- PUT /api/courses/:id 

- DELETE /api/courses/:id 
