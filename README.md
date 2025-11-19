# ♻️ sKrapy – Digital Scrap Management Ecosystem

sKrapy is a full-stack platform built to modernize and digitize the scrap ecosystem in India.  
It connects users with **verified scrap vendors**, automates **order processing**, performs **geospatial vendor matching**, and enables **secure Web3-based payments** — all through a clean, fast, and scalable interface.

This project includes separate dashboards for **users** and **vendors**, backed by a robust PostgreSQL architecture designed to handle real-world scrap operations at scale.

---

## 🚀 Key Features

### 👤 User Features
- Create account, login & email verification  
- Browse scrap categories & estimated prices  
- Place pickup requests with address + zip code  
- Automatic assignment to nearest verified vendor  
- Track pickup status  
- Reset/Forgot password flows  

### 🛠️ Vendor Features
- Vendor login + verification workflow  
- Real-time list of incoming pickup orders  
- Accept/Reject pickup requests  
- Manage profile & service areas  
- Dashboard for completed and pending orders  

### 🌐 Platform Features
- **Geo-spatial matching system**  
  Matches users with nearest vendors using zip-code clustering and optimized queries.

- **Web3 Payments (Phantom, MetaMask)**  
  Enables secure, transparent transactions using blockchain wallets.

- **PostgreSQL Backend**  
  Designed with relational models for:
  - users  
  - vendors  
  - service areas  
  - scrap orders  
  - transaction records  

- **Modern UI** built using Next.js + TypeScript  
  Responsive, fast, animation-friendly.

---

## 🏗️ Tech Stack

### **Frontend**
- Next.js (App Router)
- TypeScript
- Tailwind CSS
- React Context / Hooks
- Axios (API integration)

### **Backend**
- Node.js / Express
- PostgreSQL
- Prisma ORM (if applicable — update if different)
- JWT Authentication
- Bcrypt for hashing

### **Web3**
- MetaMask Integration  
- Phantom Wallet Integration  
- On-chain transaction verification

---

## 📂 Project Structure
sKrapy/
│── backend/ # Node.js + PostgreSQL backend
│── frontend/ # Next.js + TypeScript frontend
│── .gitignore
└── README.md

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/ShobhitChola/sKrapy-.git
cd sKrapy
```

### 🖥️ Run the Frontend
```bash
cd frontend
npm install
npm run dev
```

### ⚙️ Run the Backend
```bash
cd backend
npm install
npm start
```

### 🔐 Environment Variables
Frontend (/frontend/.env)
```bash
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_SOLANA_RPC_URL=YOUR_RPC_URL
```

Backend (/backend/.env)
```bash
DATABASE_URL=postgres://username:password@localhost:5432/skrapy
JWT_SECRET=your_secret
PORT=5000
```

## 🧪 Features Implemented in Depth

### 🔍 Geospatial Vendor Matching
Users are matched to vendors based on zip code proximity
Optimized SQL queries for location clusters
Ensures fastest pickup and lowest logistics cost

### 🔐 Secure Authentication Flow
JWT-based login for users & vendors
Encrypted passwords
Full forgot & reset password flow
Email validation steps

### 💸 Web3 Payments

MetaMask & Phantom wallet integration
Client-side signature verification
On-chain payment confirmation
Transaction recorded in the backend database
