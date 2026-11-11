
# JobTrack — Project Overview

## 1. Project Introduction

JobTrack is a full-stack job application management
system designed to help job seekers organize and
track their job applications through a centralized
platform.

## 2. Problem Statement

Job seekers often apply to multiple companies
through different platforms. Managing application
details, tracking statuses, remembering interview
dates, and monitoring progress can become difficult.

## 3. Proposed Solution

JobTrack provides a centralized dashboard where
users can securely manage their job applications,
update application statuses, schedule interviews,
and monitor their job-search progress.

## 4. Target Audience

- Fresh graduates
- University students
- Job seekers
- Professionals seeking new opportunities

## 5. Core Features

- User registration and login
- Secure user authentication
- Personal dashboard
- Job application management
- Create, view, update and delete applications
- Application status tracking
- Interview scheduling
- Application notes
- Search and filtering
- Dashboard statistics

## 6. Technology Stack

Frontend:
- React.js
- Vite
- Tailwind CSS
- React Router
- Axios

Backend:
- Python
- Flask
- Flask REST API
- SQLAlchemy

Database:
- PostgreSQL

Development and Testing:
- Git
- GitHub
- Postman
- Pytest

## 7. Main Database Entities

1. User
2. JobApplication
3. Interview
4. ApplicationNote

## 8. Project Architecture

JobTrack follows a client-server architecture.

The React frontend communicates with the Flask
backend through REST API endpoints.

The backend handles authentication, validation,
business logic, and database operations through
SQLAlchemy and PostgreSQL.

## 9. Project Goal

To develop a responsive, secure, and functional
full-stack web application demonstrating frontend
development, backend API development, database
management, authentication, testing, and deployment.

## 10. Project Scope

The application will initially focus on individual
job seekers managing their own job applications.

Each authenticated user will only be able to access
and manage their own records.
