# 🛒 Cartify

# MERN eCommerce Platform

A modern full-stack eCommerce application built with the **MERN Stack**. Cartify provides a complete online shopping experience with secure authentication, product management, shopping cart, order management, PayPal payments, and an admin dashboard.

---

## 🚀 Project Overview

Cartify is a feature-rich eCommerce platform where customers can browse products, search items, add products to their cart, place orders, and make secure online payments. Administrators can manage products, users, and customer orders through a dedicated admin panel.

---

## ⚙️ Tech Stack

| Layer | Technology |
|--------|------------|
| Frontend | React.js |
| Backend | Node.js + Express.js |
| Database | MongoDB |
| State Management | Redux Toolkit + RTK Query |
| Authentication | JWT + HTTP Only Cookies |
| Payments | PayPal |
| Styling | React Bootstrap / Bootstrap |

---

# ✨ Features

## ✅ User Features

- User Registration & Login
- Secure JWT Authentication
- User Profile Management
- Product Search
- Product Pagination
- Product Reviews & Ratings
- Top Rated Products Carousel
- Shopping Cart
- Shipping Address Management
- Checkout Process
- PayPal Payment Integration
- Order History
- Responsive Design

---

## ✅ Admin Features

- Admin Dashboard
- Product Management (CRUD)
- User Management
- Order Management
- Mark Orders as Delivered
- Upload Product Images

---

## 📁 Folder Structure

```
project-root/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── screens/
│   │   ├── slices/
│   │   ├── utils/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── data/
│   ├── server.js
│   └── package.json
│
├── uploads/
├── README.md
└── package.json
```

---

# ⚙️ Setup Instructions

## Prerequisites

- Node.js (v16 or above)
- MongoDB (Local or Atlas)
- npm

---

## 📥 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/cartify.git

cd cartify
```

---

### 2️⃣ Install Backend Dependencies

```bash
npm install
```

---

### 3️⃣ Install Frontend Dependencies

```bash
cd frontend

npm install
```

---

### 4️⃣ Configure Environment Variables

Create a `.env` file inside the root directory.

```env
NODE_ENV=development

PORT=5000

MONGO_URI=Your MongoDB Connection String

JWT_SECRET=YourSecretKey

PAYPAL_CLIENT_ID=YourPayPalClientID

PAGINATION_LIMIT=8
```

---

## ▶️ Running the Application

### Run Frontend & Backend Together

```bash
npm run dev
```

### Run Backend Only

```bash
npm run server
```

### Build Frontend

```bash
cd frontend

npm run build
```

---

# 📡 API Documentation

## Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/users/login` | Login User |
| POST | `/api/users` | Register User |
| POST | `/api/users/logout` | Logout User |
| GET | `/api/users/profile` | Get User Profile |
| PUT | `/api/users/profile` | Update Profile |

---

## Products

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Get All Products |
| GET | `/api/products/:id` | Get Product Details |
| POST | `/api/products` | Create Product (Admin) |
| PUT | `/api/products/:id` | Update Product |
| DELETE | `/api/products/:id` | Delete Product |

---

## Orders

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/orders` | Create Order |
| GET | `/api/orders/:id` | Get Order Details |
| PUT | `/api/orders/:id/pay` | Update Payment Status |
| PUT | `/api/orders/:id/deliver` | Mark Order Delivered |

---

# 💳 Payment Integration

Cartify supports secure online payments using **PayPal Checkout**.

Features include:

- Secure PayPal Transactions
- Order Payment Status
- Payment Verification

---

# 🌐 Deployment Guide

## Deploy Backend

You can deploy the backend using:

- Render
- Railway
- VPS
- Docker

Ensure:

- MongoDB Atlas URI configured
- JWT Secret configured
- PayPal Client ID configured
- Environment Variables added

---

## Deploy Frontend

Deploy using:

- Vercel
- Netlify

Set the production API URL in your frontend configuration.

---

# 🌍 MongoDB Atlas

1. Create a MongoDB Atlas Cluster
2. Create a Database User
3. Whitelist your IP Address
4. Copy the Connection String
5. Replace `MONGO_URI` inside `.env`

---


# ✅ Project Status

- ✔ User Authentication
- ✔ Product Listing
- ✔ Product Search
- ✔ Product Reviews
- ✔ Shopping Cart
- ✔ Checkout Process
- ✔ PayPal Integration
- ✔ Order Management
- ✔ Admin Dashboard
- ✔ User Management
- ✔ Product Management
- ✔ Responsive UI

---

# 📄 License

MIT License © 2026 Kanchan Sain
