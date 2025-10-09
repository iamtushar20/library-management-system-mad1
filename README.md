# Library Management System

An **Library Management System** built with **Flask**, allowing admins to manage library sections and books, while users can browse, request, and purchase books. The application includes a responsive dashboard with analytics, interactive charts, and user-friendly features.

[Watch Demo Video](https://youtu.be/CwYJEzy__9k)

---

## Table of Contents

- [Features](#features)  
- [Technologies Used](#technologies-used)  
- [Database Schema](#database-schema)  
- [Architecture](#architecture)  
- [Routes](#routes)  
- [Charts and Analytics](#charts-and-analytics)  
- [Installation](#installation)  
- [Usage](#usage)  
- [License](#license)  

---

## Features

### Admin
- Perform CRUD operations on **Sections** and **Books**.  
- View all books, sections, book requests, issue history, and user feedback.  
- Accept or deny book requests and manage book access.  
- Dashboard for analytics and insights with **charts and graphs**.  

### User
- Register, login, and manage profile.  
- Browse sections and books.  
- Request or buy books online.  
- View book issue history and manage issued books.  
- Return books and provide feedback.  
- Search for books and sections by name, author, or section.

---

## Technologies Used
- **Flask** – Python web framework for handling routes and user requests.  
- **Flask-SQLAlchemy** – ORM for database management.  
- **Jinja2** – Templating engine for dynamic HTML content.  
- **Bootstrap** – Responsive styling for forms, tables, and buttons.  
- **Chart.js** – Interactive charts for dashboard analytics.  

---

## Database Schema

### User Table
- `id`, `username`, `password`, `name`, `is_admin`  
- Stores user details and book request associations.  

### Section Table
- `id`, `name`, `creation_date`, `description`  
- Represents different sections in the library.  

### Book Table
- `id`, `name`, `content`, `authors`, `date_added`, `price`, `section_id`  
- Contains all books in the library linked to a specific section.  

### BookRequest Table
- `id`, `user_id`, `book_id`, `request_date`, `return_date`, `status`  
- Tracks requests made by users to borrow books.  

### BookIssue Table
- `id`, `user_id`, `book_id`, `authors`, `issue_date`, `return_date`, `status`, `feedback`  
- Records issued books, approval status, and user feedback.  

---

## Architecture
- `app.py` – Initializes the Flask app, sets up the database, and imports routes.  
- `routes.py` – Defines all routes for users and admins, handles HTTP requests, and interacts with the database.  
- `models.py` – Defines database models using Flask-SQLAlchemy with table relationships.  

---

## Routes

### Authentication
- Register, Login, Logout, Profile  

### Admin Routes
- CRUD for Sections and Books  
- View all Books, Sections, Book Requests, Issue History, Feedback  
- Accept/Deny Book Requests and Revoke Access  
- Dashboard with analytics  

### User Routes
- Browse, Request, and Buy Books  
- View and manage issued books  
- Return books and provide feedback  
- Search by Section, Book, or Author  

---

## Charts and Analytics
- **Bar Chart:** Number of records in each model (User, Section, Book, BookRequest, BookIssue)  
- **Top 5 Books Chart:** Most issued books  
- **Pie Chart:** Distribution of books in each section  

---

## Installation
1. Clone the repository:  
   ```bash
   git clone <repository-url>
