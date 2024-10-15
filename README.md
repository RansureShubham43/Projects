Placement Admin System
Overview
The Placement Admin System is a web-based application developed to streamline the placement process in academic institutions. It allows administrators, students, and companies to manage their roles effectively in the placement process. The system ensures a smooth workflow by automating company job postings, student registrations, and placement results.

Features
Admin Dashboard: Manage placement drives, company job postings, and student applications.
Company Module: Post job opportunities, view applications, and shortlist students.
Student Module: Register, apply for jobs, and track placement status.
Role-Based Access Control: Secure access for admins, students, and companies.
Real-Time Notifications: Email and in-app notifications for important events.
Technologies Used
Backend:
Java 8
Spring Boot 2.x
Spring Data JPA (Hibernate)
Spring Security (JWT Authentication)
Frontend:
HTML, CSS, JavaScript, Thymeleaf
Database:
MySQL
Build Tool:
Maven
Version Control:
Git
Deployment:
Tomcat
Modules
Admin Module:
Manage company job postings, schedule placement drives, and view placement results.
Student Module:
Register and apply for jobs, view placement results.
Company Module:
Post job opportunities and view student applications.
Security:
Role-based access control using Spring Security and JWT for secure endpoints.
Prerequisites
To run this project locally, you will need the following installed on your system:

Java 8 or higher
Maven
MySQL or any relational database
Git
Installation Instructions
Clone the repository from GitHub:
bash
Copy code
git clone https://github.com/your-username/placement-admin-system.git
Navigate to the project directory:
bash
Copy code
cd placement-admin-system
Configure the database:
Open the src/main/resources/application.properties file.
Update the database URL, username, and password:
properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password
Create the database schema in MySQL before starting the application:
sql
Copy code
CREATE DATABASE placement_admin;
Build the project using Maven:
bash
Copy code
mvn clean install
Run the application:
bash
Copy code
mvn spring-boot:run
The application will start on http://localhost:8080.
Database Schema
The application uses the following database tables:

students: Stores student details.
companies: Stores company details.
applications: Stores job applications by students.
placement_drives: Stores placement drive schedules.
API Endpoints
Admin:
GET /api/companies - Fetch all companies.
POST /api/companies - Add a new company.
POST /api/placements - Schedule a placement drive.
Student:
GET /api/students - Get all students.
POST /api/students/register - Register a new student.
POST /api/students/{id}/apply/{jobId} - Apply for a job.
Company:
POST /api/jobs - Post a new job.
GET /api/applicants/{jobId} - View applicants for a job.
