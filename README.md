# Node Auth MongoDB

Simple authentication system built with **Node.js**, **Express**, and **MongoDB**.
This project demonstrates how to implement **user registration, login, and authentication** using a backend API.

## 🚀 Features

* User Registration
* User Login
* Password Hashing with bcrypt
* Authentication using JSON Web Token (JWT)
* MongoDB Database Integration
* RESTful API structure

## 🛠️ Tech Stack

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**
* **bcrypt**
* **jsonwebtoken**
* **dotenv**

## 📂 Project Structure

```
node-auth-mongodb
│
├── config
│   └── db.js
│
├── controllers
│   ├── authController.js
│   └── userController.js
│
├── models
│   └── User.js
│
├── routes
│   ├── authRoutes.js
│   └── UserRoutes.js
│
├── middleware
│   ├── authMiddleware.js
│   └── errorHandler.js
├── .gitignore
├── package.json
├── app.js
├── server.js
└── README.md
```

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/MAgSAsli/node-auth-mongodb.git
```

Go to project directory

```bash
cd node-auth-mongodb
```

Install dependencies

```bash
npm install
```

Create `.env` file

```
PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
```

Run the server

```bash
npm run dev
```

or

```bash
node server.js
```

## 📡 API Endpoints

### Register User

```
POST /api/auth/register
```

Body Example

```json
{
  "username": "agil",
  "email": "agil@example.com",
  "password": "123456"
}
```

---

### Login User

```
POST /api/auth/login
```

Body Example

```json
{
  "email": "agil@example.com",
  "password": "123456"
}
```

---

## 🔐 Authentication

After login, the server will return a **JWT Token**.

Example response:

```json
{
  "token": "your_jwt_token"
}
```

Use the token in request headers:

```
Authorization: Bearer <token>
```

---

## 📌 Future Improvements

* Refresh Token
* Email Verification
* Password Reset
* Rate Limiting
* Role Based Authorization

## 👨‍💻 Author

**Moch. Agil Sugiarto**

* GitHub: https://github.com/MAgSAsli

## 📄 License

This project is licensed under the MIT License.
