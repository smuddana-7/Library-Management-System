# 📚 Library Management System

A full-stack web application for managing library operations including user registration, book check-ins/check-outs, reservations, fine payments, and more.

---

## 🚀 Tech Stack

| Layer      | Technology                     |
|------------|--------------------------------|
| Frontend   | Angular 15                     |
| Backend    | Node.js, Express.js            |
| Database   | MongoDB + Mongoose             |
| Auth       | JWT-based Authentication       |
| Communication | RESTful APIs               |

---

## 📁 Project Structure

```
library-management-system/
├── backend/               # Node.js backend
│   ├── models/            # Mongoose schemas
│   ├── routes/            # Express API routes
│   ├── server.js          # App entry
│   └── package.json
└── frontend/              # Angular frontend
    ├── src/
    ├── angular.json
    └── package.json
```

---

## 🔧 Backend Setup (`/backend`)

### 1. Install dependencies

```bash
cd backend
npm install
```

### 2. Configure MongoDB

Edit `routes/api.js` and replace the Mongo URI:

```js
const db = 'mongodb+srv://<username>:<password>@cluster.mongodb.net/library_management_system';
```

### 3. Start server

```bash
node server.js
```

Runs on `http://localhost:5000`.

---

## 💡 Backend Features

- User Registration & Login (JWT Auth)
- Library creation and listing
- Book CRUD (Add, Delete, View by Library)
- Check-in / Check-out flow
- Reservation handling
- Fine calculation and payments
- Role-based access and filters

---

## 🌐 Frontend Setup (`/frontend`)

### 1. Install dependencies

```bash
cd frontend
npm install
```

### 2. Start the Angular Dev Server

```bash
ng serve
```

Runs on `http://localhost:4200`

### 3. Build for Production

```bash
ng build
```

---

## 🔐 Authentication

- JWT token returned on login/register
- Pass token in `Authorization` header for secured routes

```http
Authorization: Bearer <your_token>
```

---

## 📬 API Summary

| Feature         | Method | Endpoint                 |
|----------------|--------|--------------------------|
| Register/Login | POST   | `/api/register` `/login` |
| Libraries      | GET/POST | `/api/library-list` `/add-library` |
| Books          | GET/POST | `/api/book-list` `/add-book` |
| Transactions   | POST   | `/api/check-in` `/check-out` `/renewal-book` |
| Reservations   | GET/POST/DELETE | `/api/reserve-book` |
| Fines          | GET/POST | `/api/fine-list` `/pay-fine` |

---

## ✅ To Do

- ✅ Full check-in/check-out lifecycle
- ✅ Reservation management
- ✅ Fine processing
- 🔲 Admin dashboard
- 🔲 Email notifications
