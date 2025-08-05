# Login Page Project

This is a simple full-stack login form project using **HTML + Tailwind CSS** on the frontend, **Node.js (Express)** for the backend, and **MySQL** as the database. User input (email and password) is submitted from a form and stored securely in a MySQL database.

---

## 🚀 Features

- Tailwind CSS via CDN for fast, responsive design
- Express.js server with POST route to handle form submission
- MySQL database connection using `mysql2`
- Environment variables managed with `.env`
- Stores email & password in MySQL `users` table
- Optional GET endpoint to view all users in JSON

---

## 🛠 Technologies Used

- HTML + Tailwind CSS (CDN)
- Node.js & Express
- MySQL (via XAMPP or standalone)
- npm packages: `express`, `dotenv`, `body-parser`, `mysql2`

---

## 📁 Folder Structure

```
project-root/
├── public/
│   └── index.html        # Frontend login form
├── .env                  # Environment variables (not pushed)
├── .gitignore            # Ignores node_modules and .env
├── server.js             # Backend server code
└── package.json
```

---

## 📦 Installation

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
npm install
```

Create a `.env` file:
```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=       # Leave blank if no password
DB_NAME=logindb
PORT=3000
```

Make sure your MySQL server is running and a `logindb` database with a `users` table exists:

```sql
CREATE DATABASE logindb;
USE logindb;
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  email VARCHAR(255),
  password VARCHAR(255)
);
```

---

## ▶️ Run the Project

```bash
node server.js
```

Visit in browser:
```
http://localhost:3000/index.html
```

Submit the form to insert data into MySQL. To view all users (optional):
```
http://localhost:3000/users
```

---

## 📄 License

This project is for educational/demo purposes. Feel free to use and modify.
