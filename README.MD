# 🗳️ Voting Application API

A secure and scalable RESTful backend API for an online voting system built with Node.js, Express.js, and MongoDB. The application enables users to register, authenticate, view candidates, and cast votes while providing administrative controls for candidate management.

## 🚀 Features

### User Authentication

* Secure user registration using Aadhaar Card Number and password
* JWT-based authentication and authorization
* Protected API routes
* Password management functionality

### Voting System

* View all available candidates
* Cast a vote for a preferred candidate
* One vote per registered user
* Prevents duplicate voting

### Candidate Management (Admin Only)

* Add new candidates
* Update candidate details
* Delete candidates
* Monitor voting statistics

### User Profile

* View profile information
* Change account password securely

## 🛠️ Tech Stack

* **Backend:** Node.js, Express.js
* **Database:** MongoDB, Mongoose
* **Authentication:** JSON Web Token (JWT)
* **Environment Variables:** dotenv
* **Password Encryption:** bcrypt.js

## 📂 Project Repository

Repository: https://github.com/Rahul70079/Nodejs-voting-api

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Rahul70079/Nodejs-voting-api.git
```

### 2. Navigate to the Project Directory

```bash
cd Nodejs-voting-api
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and add:

```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=3000
```

### 5. Start the Application

```bash
npm start
```

The server will run on:

```bash
http://localhost:3000
```

## 📌 API Endpoints

### Authentication

| Method | Endpoint | Description                        |
| ------ | -------- | ---------------------------------- |
| POST   | /signup  | Register a new user                |
| POST   | /login   | Authenticate user and generate JWT |

### Candidates

| Method | Endpoint        | Description                           |
| ------ | --------------- | ------------------------------------- |
| GET    | /candidates     | Retrieve all candidates               |
| POST   | /candidates     | Add a candidate (Admin Only)          |
| PUT    | /candidates/:id | Update candidate details (Admin Only) |
| DELETE | /candidates/:id | Delete a candidate (Admin Only)       |

### Voting

| Method | Endpoint               | Description                        |
| ------ | ---------------------- | ---------------------------------- |
| GET    | /candidates/vote/count | Get vote counts for all candidates |
| POST   | /candidates/vote/:id   | Vote for a candidate               |

### User Profile

| Method | Endpoint                | Description                      |
| ------ | ----------------------- | -------------------------------- |
| GET    | /users/profile          | Get authenticated user's profile |
| PUT    | /users/profile/password | Update user password             |

## 🔒 Security Features

* JWT Authentication
* Password Hashing with bcrypt
* Role-Based Access Control (Admin/User)
* Protected Routes
* Vote Duplication Prevention

## 📈 Future Enhancements

* Email Verification
* Election Scheduling
* Real-Time Voting Statistics
* Audit Logs
* Admin Dashboard
* API Documentation with Swagger

## 👨‍💻 Author

**Rahul Kumar**

If you found this project helpful, consider giving it a ⭐ on GitHub.
