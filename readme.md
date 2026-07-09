# Cartify eCommerce Platform 🛒✨

Welcome to **Cartify**, my first major milestone project as a full-stack developer! Built using the **MERN Stack** (MongoDB, Express, React, Node.js) and managed with **Redux Toolkit**, this application represents my best effort to learn, build, and deploy a full-featured, secure e-commerce application from scratch.

This project represents not just code, but hours of debugging, learning modern state management, understanding server architecture, and breaking through common development bottlenecks.

---

## 🚀 Key Features Implemented

* **Complete Shopping Pipeline:** Interactive product detail views, dynamic quantities, local-storage-backed shopping cart states, and structured multi-step checkout processes (Shipping → Payment → Place Order).
* **Secure Cookie Authentication:** Implemented JSON Web Token (JWT) storage utilizing secure `HttpOnly` browser cookies to manage sessions safely.
* **State-of-the-Art State Management:** Integrated **Redux Toolkit RTK Query** to handle clean asynchronous server interactions, data pre-fetching, and cache validation hooks.
* **Full Admin Suite:** Robust management dashboards for managing products, auditing global user records, and updating individual fulfillment delivery states.
* **External Payment Systems:** Native integration with the PayPal JavaScript SDK for secure transaction testing.
* **Product Discovery Slices:** Custom server-side database pagination limits, full-text keyword regex searching, and an elegant "Top Rated" product showcase carousel.

---

## 🛠️ The Tech Stack

* **Frontend:** React.js (v18), React Bootstrap (UI Framework), Redux Toolkit (RTK Query), React Router DOM.
* **Backend:** Node.js, Express.js, Multer (Local Media Upload Pipeline).
* **Database:** MongoDB Atlas via the Mongoose ODM framework.
* **Payment APIs:** PayPal Sandbox Environment.

---

## 🧠 Lessons Learned & Challenges Overcome

Building this project taught me that engineering is 20% writing code and 80% troubleshooting. Some of my biggest learning breakthroughs included:

1.  **The HTTP-Only Cookie Trap (`credentials: 'include'`):** I spent a long time diagnosing why users couldn't stay signed in. I discovered that when using strict HTTP-Only cookies, browsers automatically block them from traveling across local development ports unless `credentials: 'include'` is explicitly declared inside the RTK query wrapper.
2.  **Resolving `EADDRINUSE` Port Conflicts on macOS:** When setting up my local proxy environment on port `5000`, the server repeatedly crashed. I learned that macOS uses port 5000 natively for its AirPlay Receiver service. Learning to systematically locate active system threads, kill ghost processes, and smoothly redirect my application's pipeline proxy bridge to port `5001` was a massive lesson in system infrastructure.
3.  **Client/Server Price Validation (Security First):** I learned never to trust prices submitted directly by the client browser code. My backend order controller intercepts the cart items array, queries the actual values straight from the MongoDB collection, and processes calculations securely on the server side to prevent request manipulation.

---

## 🔧 Installation and Local Setup

### 1. Environment Configuration
Create a `.env` file in your **backend root folder** and populate it with your environment keys:

```env
PORT=5001
NODE_ENV=development
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_custom_secure_jwt_secret_string
PAGINATION_LIMIT=3

# PayPal Sandbox Credentials
PAYPAL_CLIENT_ID=your_paypal_sandbox_client_id
