# ⚙️ E-Commerce Application - Backend API

![Status](https://img.shields.io/badge/status-active-success)
![Stack](https://img.shields.io/badge/stack-Node.js%20%2B%20Express-green)
![Database](https://img.shields.io/badge/database-MongoDB-brightgreen)
![License](https://img.shields.io/badge/license-MIT-orange)

> REST API backend for the E-Commerce application — handles authentication, product management, persistent cart operations, address management, and complete order processing using Node.js, Express, and MongoDB.

---

## 🌐 Live Demo

| Frontend App | Frontend Repo |
|---|---|
| [ecom-two-virid.vercel.app](https://ecom-two-virid.vercel.app/) | [GitHub Frontend](https://github.com/vaibhavkumar18/Ecom) |

---

## 📌 Overview

This is the backend service for the E-Commerce application. It exposes RESTful APIs consumed by the React frontend. The backend handles user authentication, product data, cart persistence, address management, and order placement.

**Key Highlights:**
- JWT-based secure authentication with protected routes
- Persistent shopping cart stored in MongoDB
- Complete order placement and checkout flow
- Address management with add, edit, and delete
- Modular MVC architecture with separate controllers, models, and routes

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Framework | Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcrypt |
| Dev Tools | Nodemon, dotenv, CORS, cookie-parser |

---

## 🧠 Features

- ✅ User registration and login with JWT authentication
- ✅ Protected routes via auth middleware
- ✅ Dynamic product listing and detail APIs
- ✅ Persistent cart stored in MongoDB across sessions
- ✅ Add, remove, and update quantity in cart
- ✅ Complete order placement and retrieval
- ✅ Address management — add, edit, delete
- ✅ Modular MVC backend architecture
- ✅ CORS configured for frontend communication

---


---

## 🔗 Related Repository

🖥️ Frontend repo:
👉 [github.com/vaibhavkumar18/Ecom](https://github.com/vaibhavkumar18/Ecom)

---

## 🚀 Getting Started

### 1. Clone Repository
```bash
git clone https://github.com/vaibhavkumar18/Ecom-backend.git
cd Ecom-backend
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment Variables
Create a `.env` file in the root:
```env
PORT=3000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
FRONTEND_URL=your_frontend_url
NODE_ENV=development
```

### 4. Run Backend
```bash
# Development
npm run dev

# Production
npm start
```

---

## 📡 API Reference

### Auth Routes
| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| POST | /api/auth/register | Register new user | ❌ |
| POST | /api/auth/login | Login user | ❌ |
| GET | /api/auth/get-me | Get current user | ✅ |

### Product Routes
| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | /api/products | Get all products | ❌ |
| GET | /api/products/:id | Get single product | ❌ |

### Cart Routes
| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | /api/cart | Get user cart | ✅ |
| POST | /api/cart/add | Add item to cart | ✅ |
| PUT | /api/cart/update | Update item quantity | ✅ |
| DELETE | /api/cart/remove/:id | Remove item from cart | ✅ |

### Order Routes
| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| POST | /api/orders/place | Place order | ✅ |
| GET | /api/orders | Get user orders | ✅ |

### Address Routes
| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | /api/address | Get all addresses | ✅ |
| POST | /api/address/add | Add new address | ✅ |
| PUT | /api/address/update/:id | Update address | ✅ |
| DELETE | /api/address/delete/:id | Delete address | ✅ |

---

## 🔐 How Authentication Works

1. User registers or logs in
2. Backend signs a **JWT token** and returns it
3. Frontend stores token and sends it with every protected request
4. Auth middleware verifies token on all protected routes
5. Invalid or missing token returns 401 Unauthorized

---

## 👨‍💻 Author

**Vaibhav Kumar Nigam**
- 🔗 LinkedIn: [linkedin.com/in/vaibhavcodes](https://www.linkedin.com/in/vaibhavcodes)
- 🐙 GitHub: [github.com/vaibhavkumar18](https://github.com/vaibhavkumar18)
- 📧 Email: vaibhavkumarnigam30@gmail.com

---

⭐ Found this project helpful? A star would mean a lot!
