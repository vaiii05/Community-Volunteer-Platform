<div align="center">

# 🤝 Community Volunteer Platform

**A full-stack MERN platform that connects volunteers with local NGOs and makes organizing community events effortless.**

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

</div>

---

## 📌 The Problem

NGOs struggle to find the right volunteers for their events, and willing volunteers don't know where help is needed. Coordination ends up scattered across WhatsApp groups and spreadsheets.

This platform brings both sides into one place: NGOs register and post events, volunteers discover and join them, and **matching logic surfaces the events that fit each volunteer best.**

## ✨ Features

| For Volunteers | For NGOs |
|---|---|
| Secure sign-up and login | Organization registration and profile |
| Browse and search upcoming events | Create, edit and manage events |
| Personalized event matches based on skills and interests | View and manage volunteer applicants |
| One-click apply / RSVP | Track participation per event |

**Platform-wide:** JWT authentication · role-based access (Volunteer / NGO) · responsive UI · REST API

## 🧠 How Event Matching Works

1. Each **event** lists its required skills, location and date.
2. Each **volunteer profile** lists skills, interests and availability.
3. The matching logic scores the overlap between the two and ranks events for each volunteer, so the most relevant opportunities appear first.

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js, TypeScript, CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JSON Web Tokens (JWT), bcrypt |
| Tools | Git, GitHub, Postman |

## 🏗️ Architecture

```
React Client  ──►  REST API (Express + Node.js)  ──►  MongoDB
   (UI)             (auth, events, matching)         (users, orgs, events)
```

## 🚀 Getting Started

**Prerequisites:** Node.js 18+, npm, and a MongoDB instance (local or Atlas).

```bash
# 1. Clone the repository
git clone https://github.com/vaiii05/Community-Volunteer-Platform.git
cd Community-Volunteer-Platform

# 2. Install backend dependencies
cd server
npm install

# 3. Install frontend dependencies
cd ../client
npm install
```

**Environment variables:** create a `.env` file inside `server/`:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

**Run the app** (two terminals):

```bash
# Terminal 1: backend
cd server && npm run dev

# Terminal 2: frontend
cd client && npm start
```

Open **http://localhost:3000** 🎉

## 🔌 API Overview

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a volunteer or NGO |
| POST | `/api/auth/login` | Log in and receive a JWT |
| GET | `/api/events` | List all events |
| POST | `/api/events` | Create an event (NGO only) |
| POST | `/api/events/:id/apply` | Apply to an event (Volunteer) |
| GET | `/api/events/matches` | Get events ranked for the logged-in volunteer |

## 📁 Project Structure

```
Community-Volunteer-Platform/
├── client/          # React frontend
│   └── src/
│       ├── components/
│       ├── pages/
│       └── services/
├── server/          # Express backend
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   └── middleware/
└── README.md
```

<!--
## 📸 Screenshots
Add images to a docs/ folder, then uncomment:

| Home | Event Matches | NGO Dashboard |
|---|---|---|
| ![Home](docs/home.png) | ![Matches](docs/matches.png) | ![Dashboard](docs/dashboard.png) |
-->

## 🗺️ Roadmap

- [ ] Email notifications for new matches and applications
- [ ] Map-based event search by location
- [ ] Admin dashboard for verifying NGOs
- [ ] Automated tests and CI

## 👥 Team

- **Vaibhavi Rai** ([@vaiii05](https://github.com/vaiii05)): authentication, organization registration, event-matching logic
- **Arnav Rade** ([@ArnavRade](https://github.com/ArnavRade))

## 📬 Contact

**Vaibhavi Rai** · [GitHub](https://github.com/vaiii05) · [LinkedIn](https://www.linkedin.com/in/vaibhavi-rai-2b6110357/) · vaibhavii.0515@gmail.com

---
<div align="center">⭐ If you like this project, give it a star!</div>
