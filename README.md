# Task Manager System

A web-based Task Management System built with Laravel to help users organize, manage, and track their daily tasks efficiently.

---

## Overview

The Task Manager System is designed to improve productivity by providing a structured platform for managing tasks. Users can create tasks, update them, track their status, set priorities, and manage deadlines in a secure environment.

The system follows the MVC (Model-View-Controller) architecture and includes authentication, authorization, and ownership-based task protection.

---

## Features

- User Registration and Login
- Email Verification
- Password Reset
- Create Tasks
- Edit Tasks
- Delete Tasks
- View Task Details
- Search Tasks
- Filter Tasks by Status
- Filter Tasks by Priority
- Task Status Tracking
- Task Priority Management
- Due Date Management
- Overdue Task Checking Logic
- Dashboard Statistics
- Profile Management
- Ownership Protection Middleware

---

## Technologies Used

- **Laravel**
- **PHP**
- **MySQL**
- **Blade Templates**
- **Tailwind CSS**
- **Laravel Breeze**
- **Middleware**
- **Eloquent ORM**

---

## System Architecture

This project follows the MVC Architecture:

- **Model** → Handles database operations
- **View** → Handles user interfaces
- **Controller** → Handles business logic

---

## Database Design

### Users Table

| Column | Type |
|---|---|
| id | Primary Key |
| name | String |
| email | String |
| password | String |
| created_at | Timestamp |
| updated_at | Timestamp |

---

### Tasks Table

| Column | Type |
|---|---|
| id | Primary Key |
| user_id | Foreign Key |
| title | String |
| description | Text |
| status | Enum |
| priority | Enum |
| due_date | Date |
| created_at | Timestamp |
| updated_at | Timestamp |

---

## Relationships

- A **User** can have many **Tasks**
- A **Task** belongs to one **User**

---

## Security Features

- Authentication using Laravel Breeze
- Email Verification
- Route Protection with Middleware
- Ownership Validation using `EnsureTaskOwner`
- Input Validation
- CSRF Protection

---

## Installation

### Clone the repository

```bash
git clone https://github.com/safaabd2026/task-manager.git
```

### Navigate to project directory

```bash
cd task-manager
```

### Install dependencies

```bash
composer install
npm install
```

### Configure environment

```bash
cp .env.example .env
```

### Generate application key

```bash
php artisan key:generate
```

### Configure database in `.env`

```env
DB_DATABASE=task_manager
DB_USERNAME=root
DB_PASSWORD=
```

### Run migrations

```bash
php artisan migrate
```

### Start development server

```bash
php artisan serve
npm run dev
```

---

## Usage

1. Register a new account.
2. Verify your email.
3. Login to the system.
4. Create tasks.
5. Manage tasks.
6. Search and filter tasks.
7. Update task status.
8. Monitor task progress.

---

## Future Enhancements

- Email Notifications
- Mobile Application
- Team Collaboration
- Task Sharing
- Calendar Integration
- REST API
- Real-Time Notifications
- Task Analytics

---

## Project Structure

```text
app/
├── Http/
│   ├── Controllers/
│   ├── Middleware/
├── Models/
database/
resources/views/
routes/
config/
tests/
```



## License

This project is for educational purposes.