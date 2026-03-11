<div align="center">

# 🌍 TravelMate
### *Your All-in-One Smart Travel Companion*

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Google Maps](https://img.shields.io/badge/Google_Maps_API-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

> **A production-grade, full-stack travel booking platform — book cabs, hotels, and travel packages in one seamless interface.**
> Think MakeMyTrip, built from scratch.

---

[![Stars](https://img.shields.io/github/stars/your-username/travelmate?style=social)](https://github.com/your-username/travelmate)
[![Forks](https://img.shields.io/github/forks/your-username/travelmate?style=social)](https://github.com/your-username/travelmate)

</div>

---

## 📌 Table of Contents
- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Authors](#-authors)

---

## 🚀 About The Project

**TravelMate** is a comprehensive end-to-end travel booking platform that brings cab booking, hotel reservations, and travel package management under a single, unified interface.

Built entirely from scratch — no templates, no shortcuts — TravelMate demonstrates full-stack engineering ownership from UI design to database architecture, with real-time mapping, secure authentication, and a modular backend built to scale.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🚕 **Cab Booking** | Real-time cab search, route mapping, live ETA tracking |
| 🏨 **Hotel Reservations** | Search, filter, and book hotels with instant confirmation |
| 📦 **Travel Packages** | Browse and book curated travel packages end-to-end |
| 🗺️ **Live Route Tracking** | Google Maps API integration for real-time driver movement |
| 🔐 **Secure Authentication** | JWT-based login, session management, and protected routes |
| 📊 **User Dashboard** | Personalised dashboard showing bookings, history, and profile |

---

## 🏗️ System Architecture

```
TravelMate/
│
├── client/                  # ReactJS Frontend
│   ├── components/          # Reusable UI components
│   ├── pages/               # Cab | Hotel | Packages | Dashboard
│   └── services/            # API call handlers
│
├── server/                  # Node.js Backend
│   ├── routes/
│   │   ├── cab.routes.js    # Cab booking service
│   │   ├── hotel.routes.js  # Hotel booking service
│   │   └── package.routes.js# Travel package service
│   ├── middleware/
│   │   └── auth.js          # JWT authentication middleware
│   └── config/
│       └── db.js            # MySQL database config
│
└── database/
    └── schema.sql           # Full relational schema
```

> Each backend service is **independently deployable** — updating cab routing has zero impact on hotel or package services.

---

## 🛠️ Tech Stack

### Frontend
- **ReactJS** — Modular component architecture with clean separation of concerns
- **Google Maps API** — Live routing, ETA, and location-based search
- **Google Places API** — Real-time location autocomplete and discovery

### Backend
- **Node.js** — Decoupled, modular REST API server
- **JWT Authentication** — Secure token-based login and session handling
- **Express.js** — Lightweight routing and middleware management

### Database
- **MySQL** — Relational schema managing:
  - User profiles & authentication records
  - Cab, hotel & package booking records
  - Transaction history & route data

---

## 🗺️ Core Module — Real-Time Routing

```javascript
// Live cab routing with Google Maps Directions API
const getRoute = async (origin, destination) => {
  const response = await mapsClient.directions({
    params: {
      origin,
      destination,
      mode: "driving",
      key: process.env.GOOGLE_MAPS_API_KEY,
    },
  });
  return response.data.routes[0];
};
```

---

## 🔐 Authentication Flow

```
User Login
    ↓
Credentials verified against MySQL
    ↓
JWT Token generated (expires in 24h)
    ↓
Token stored client-side
    ↓
All protected routes validate token via middleware
    ↓
Expired/invalid token → redirect to login
```

---

## ⚡ Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/travelmate.git

# Install backend dependencies
cd server && npm install

# Install frontend dependencies
cd client && npm install

# Set up environment variables
cp .env.example .env
# Add your Google Maps API Key and MySQL credentials

# Run the backend
cd server && npm start

# Run the frontend
cd client && npm start
```

---

## 👨‍💻 Authors

<div align="center">

| Karthik G Kulkarni | Prathamesh | Raghu |
|---|---|---|
| [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/your-username) | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/prathamesh-username) | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/raghu-username) |

| Shashank | Ayush | Karthik |
|---|---|---|
| [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shashank-username) | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ayush-username) | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/karthik2-username) |

</div>

---

<div align="center">

*Built with passion, engineered with purpose.*

⭐ **Star this repo if you found it useful!** ⭐

</div>
