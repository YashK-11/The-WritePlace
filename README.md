#  The WritePlace - Notes WebApp

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

**A modern, secure, and minimalistic notes application backend built with Node.js and Express**
 
</div>

---

## Overview

The WritePlace is a full-stack notes application designed with a focus on speed, security, and simplicity.


## Features

### Current Features
-  RESTful API architecture
-  Modular and scalable codebase structure
- Environment-based configuration

## Planned Features
-     Authentication & Security
  - User registration and login
  - JWT-based authentication
  - Secure password hashing (bcrypt)
  - Session management with refresh tokens
  - Rate limiting and security headers

-     Notes Management
  - Create, read, update, and delete notes
  - User-specific note isolation
  - Pagination and filtering
  - Search functionality
  - Soft delete with restore capability

-     Security & Best Practices
  - Input validation and sanitization
  - SQL injection prevention
  - CORS configuration
  - Comprehensive error handling
  - Request logging

---

## 🚀 Tech Stack

| Technology | Purpose |
|------------|---------|
| **Node.js** | JavaScript runtime environment |
| **Express.js** | Web application framework |
| **MySQL** | Relational database management |
| **JWT** | Secure token-based authentication |
| **bcrypt** | Password hashing algorithm |
| **dotenv** | Environment variable management |


---

### File Structure :
```
the-writeplace-backend/
├── src/
│   ├── config/
│   │   ├── database.js       NEW
│   │   ├── initDB.js         NEW
│   │   └── schema.sql        NEW
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   └── app.js                UPDATED
├── .env                      UPDATED
├── .env.example
├── .gitignore
├── package.json             UPDATED
├── package-lock.json        UPDATED
└── README.md
```

---

##  Troubleshooting

### "Access denied for user 'root'@'localhost'"
```bash
# Reset MySQL root password or use correct password in .env
```

### "Cannot connect to MySQL server"
```bash
# Check if MySQL is running
# Windows: Check Services
# Mac/Linux: sudo service mysql status
```

### "Database already exists" error
```bash
# This is fine! The script handles existing databases
```

### Port 3306 already in use
```bash
# Another MySQL instance might be running
# Or change DB_PORT in .env to 3307
```
---

##  Getting Started

### Prerequisites

Make sure you have the following installed:
- **Node.js** (v16.x or higher) - [Download](https://nodejs.org/)
- **MySQL** (v8.x or higher) - [Download](https://dev.mysql.com/downloads/mysql/)
- **npm** or **yarn** package manager
- **Git** for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YashK-11/The-WritePlace.git
   cd The-WritePlace/the-writeplace-backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   # Copy the example environment file
   cp .env.example .env
   
   # Edit .env with your configuration
   ```

4. **Setup MySQL database**
   ```bash
   # Create database 
   mysql -u root -p
   CREATE DATABASE writeplace_db;
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Verify installation**
   
   Open your browser and navigate to `http://localhost:5000`
   
   You should see:
   ```json
   {
     "message": "Welcome to The WritePlace API",
     "version": "1.0.0",
     "status": "Server is running"
   }
   ```

---

## 🔧 Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=writeplace_db
DB_PORT=3306

```
---

## 📚 API Documentation

### Base URL
```
http://localhost:5000/api
```


##  Author

- GitHub: [@YashK-11](https://github.com/YashK-11)
- Project Link: [The WritePlace](https://github.com/YashK-11/The-WritePlace)

---

<div align="center">

Made with ❤️ and ☕

</div>
