# Farm-to-Table E-Commerce Platform

A full-stack e-commerce platform connecting farmers directly with consumers, featuring role-based dashboards, KYC verification, real-time chat, order management, and more.

---

## 🚀 Features

### User Roles
- **Farmer:**
  - Login via phone/email + password/OTP
  - KYC verification (Aadhar, PAN, etc.)
  - Add/manage products
  - Track orders and earnings
  - Chat with consumers
  - Sales dashboard & analytics
  - Logistics partner options
  - Fair pricing tool
- **Consumer:**
  - Login via phone/email + password/OTP
  - Simple registration & address management
  - Browse products by category
  - Track orders
  - Multiple payment options
  - Rate & review products/farmers
  - Subscription/repeat orders
  - Local produce finder

### Advanced Features
- Geo-location based services
- Digital invoicing & GST support
- Organic certification tags
- Offline support mode
- AI crop demand forecasting
- Live farm view/stories
- Community market feature

---

## 🛠 Tech Stack
- **Frontend:** React (Create React App)
- **Backend:** Node.js, Express
- **Database:** MongoDB Atlas
- **Authentication:** JWT, OTP (SMS/Email)
- **Cloud Hosting:** Vercel (frontend), Render (backend)
- **Payment Gateway:** Razorpay/Stripe (integration ready)

---

## 🏗️ Local Development Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Setup Backend
```bash
cd server
npm install
```
- Create a `.env` file in `/server` with:
  ```env
  MONGODB_URI=your_mongodb_atlas_connection_string
  JWT_SECRET=your_jwt_secret
  CLIENT_URL=http://localhost:3000
  ```
- Start the backend:
  ```bash
  npm start
  # or for development
  npm run dev
  ```

### 3. Setup Frontend
```bash
cd ../client
npm install
```
- Create a `.env` file in `/client` with:
  ```env
  REACT_APP_API_URL=http://localhost:5000
  ```
- Start the frontend:
  ```bash
  npm start
  ```

---

## 🌐 Deployment Guide

### Deploy Backend (Node.js/Express) on Render
1. Push your code to GitHub.
2. [Create a free MongoDB Atlas cluster](https://www.mongodb.com/atlas/database) and get your connection string.
3. [Sign up at Render.com](https://render.com/).
4. Create a new **Web Service**:
   - Connect your GitHub repo
   - Root directory: `/server`
   - Build command: `npm install`
   - Start command: `npm start`
   - Add environment variables:
     - `MONGODB_URI` = your MongoDB Atlas connection string
     - `JWT_SECRET` = your secret
     - `CLIENT_URL` = (your frontend URL, after deploying frontend)
5. Deploy and get your backend URL (e.g., `https://your-backend.onrender.com`)

### Deploy Frontend (React) on Vercel
1. Push your frontend code to GitHub (ensure `/client` is the root for frontend).
2. [Sign up at Vercel.com](https://vercel.com/).
3. Import your GitHub repo:
   - Root directory: `/client`
   - Build command: `npm run build`
   - Output directory: `build`
   - Add environment variable:
     - `REACT_APP_API_URL` = your Render backend URL
4. Deploy and get your frontend URL (e.g., `https://your-frontend.vercel.app`)

### Update CORS and Environment Variables
- Make sure your backend's `CLIENT_URL` matches your Vercel frontend URL.
- Make sure your frontend's `REACT_APP_API_URL` matches your Render backend URL.

---

## 📦 Folder Structure
```
root/
  client/      # React frontend
  server/      # Node.js/Express backend
```

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License
[MIT](LICENSE)
