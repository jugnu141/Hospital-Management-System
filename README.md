```markdown
# 🏥 Hospital Management System

A complete hospital management web application that allows patients to book appointments and admins to manage doctors, appointments, and messages.

## 🌐 Live Demo

| Portal | Demo Link |
|--------|-----------|
| **Patient Portal** | [lifecare-hospitals.netlify.app](https://lifecare-hospitals.netlify.app) |
| **Admin Panel** | [lifecare-administration.netlify.app](https://lifecare-administration.netlify.app) |

---

## ✨ Features

### Patient Side
- Create account and login
- Book appointments with doctors
- Send messages to hospital admin
- View hospital information

### Admin Side
- Add and manage doctors
- Approve or reject appointments
- View and reply to patient messages
- Add new admin users

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| Frontend | React.js, Bootstrap, Axios |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| Authentication | JWT, Bcrypt |
| Image Upload | Cloudinary |

---

## 📁 Folder Structure

```
Hospital-Management-System/
│
├── Backend/           # API server (Node.js + Express)
├── Frontend-Admin/    # Admin dashboard (React)
├── Frontend-Patient/  # Patient portal (React)
└── README.md
```

---

## 💻 Installation Guide

### Prerequisites

Before starting, you need:
- **Node.js** installed on your computer ([Download here](https://nodejs.org))
- **MongoDB Atlas** account ([Free signup here](https://www.mongodb.com/cloud/atlas))
- **Cloudinary** account ([Free signup here](https://cloudinary.com/))

---

### Step 1: Download the Code

```bash
git clone https://github.com/YOUR_USERNAME/Hospital-Management-System.git
cd Hospital-Management-System
```

### Step 2: Install Backend

```bash
cd Backend
npm install
```

### Step 3: Install Patient Portal

```bash
cd ../Frontend-Patient
npm install
```

### Step 4: Install Admin Panel

```bash
cd ../Frontend-Admin
npm install
```

### Step 5: Set Up Environment Variables

Create a file named `.env` inside the `Backend` folder and add:

```env
PORT=5000
MONGO_URI=mongodb+srv://your_username:your_password@cluster.mongodb.net/hospital_db
JWT_SECRET_KEY=your_secret_key_here
JWT_EXPIRES=7d
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

**How to get these values:**
- `MONGO_URI` → From MongoDB Atlas after creating a cluster
- `JWT_SECRET_KEY` → Type anything random (example: `mySecretKey12345`)
- Cloudinary values → From your Cloudinary dashboard

### Step 6: Run the Application

You need **3 separate terminal windows** open:

| Terminal | Command | Opens At |
|----------|---------|----------|
| **Terminal 1 (Backend)** | `cd Backend && npm run dev` | http://localhost:5000 |
| **Terminal 2 (Patient)** | `cd Frontend-Patient && npm run dev` | http://localhost:5175 |
| **Terminal 3 (Admin)** | `cd Frontend-Admin && npm run dev` | http://localhost:5174 |

### Step 7: Create Admin Account

1. Go to **Patient Portal** (http://localhost:5175)
2. Click **Register** and create a new account
3. Go to your **MongoDB Atlas** dashboard
4. Find the `users` collection in your database
5. Locate the account you just created
6. Change the `role` field from `"Patient"` to `"Admin"`
7. Save the changes
8. Now go to **Admin Panel** (http://localhost:5174) and login

---

## 🚀 Deployment

### Deploy Backend (Free on Render)

1. Push your code to GitHub
2. Go to [render.com](https://render.com) and sign up
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Set the following:
   - **Name:** Any name you want
   - **Root Directory:** `Backend`
   - **Start Command:** `npm start`
6. Add your environment variables in Render dashboard
7. Click "Deploy"

### Deploy Frontend (Free on Netlify)

1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the `dist` folder from your frontend projects
3. Or connect your GitHub repository

---

## 📝 Common Issues & Solutions

| Problem | Solution |
|---------|----------|
| `npm not found` | Install Node.js from nodejs.org |
| MongoDB connection error | Check your MongoDB username/password in `.env` |
| Port already in use | Change `PORT=5000` to `5001` or `5002` |
| Blank white page | Wait 30 seconds or restart the backend |
| Cannot login after registration | Check if MongoDB is connected successfully |

---

## 📄 License

This project is open source under the MIT License.

---

## 👤 Connect With Me

- GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
- Project Link: [github.com/YOUR_USERNAME/Hospital-Management-System](https://github.com/YOUR_USERNAME/Hospital-Management-System)

---

**⭐ Star this repository if you found it helpful!**
```