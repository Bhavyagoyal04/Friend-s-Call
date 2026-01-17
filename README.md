# Friend's Call (WebRTC Video Calling + Chat)

Friend's Call is a real-time video calling and chat application built using **WebRTC**, **Socket.IO**, **React**, and **Node.js**.  
Users can join a room using a meeting code (URL), connect with others, and communicate through video/audio + chat.

---

## Features

- Real-time video calling (WebRTC)
- Audio mute / unmute
- Camera on / off
- Screen sharing
- Real-time chat (Socket.IO)
- Join room using meeting code / URL
- User disconnect handling (removes from room)
- Room + chat cleanup when last user leaves

---

## Tech Stack

### Frontend
- **React.js**
- **Material UI (MUI)**
- **Socket.IO Client**
- **WebRTC**
- **CSS Modules**

### Backend
- **Node.js**
- **Express.js**
- **Socket.IO**
- **MongoDB Atlas** (Cloud Database)
- **Mongoose**
- **CORS**

### Deployment
- **Render** (Frontend + Backend hosting)

---

## Updated Project Structure

```txt
Friend's Call/
│
├── backend/
│   ├── node_modules/
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── socketManager.js
│   │   │   └── user.controller.js
│   │   │
│   │   ├── models/
│   │   │   ├── meeting.model.js
│   │   │   └── user.model.js
│   │   │
│   │   ├── routes/
│   │   │   └── users.routes.js
│   │   │
│   │   └── app.js
│   │
│   ├── package.json
│   └── package-lock.json
│
├── frontend/
│   ├── node_modules/
│   ├── public/
│   ├── src/
│   │   ├── contexts/
│   │   │   └── AuthContext.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── authentication.jsx
│   │   │   ├── history.jsx
│   │   │   ├── home.jsx
│   │   │   ├── landing.jsx
│   │   │   └── VideoMeet.jsx
│   │   │
│   │   ├── styles/
│   │   │   └── videoComponent.module.css
│   │   │
│   │   ├── utils/
│   │   │   └── withAuth.jsx
│   │   │
│   │   ├── App.css
│   │   ├── App.js
│   │   ├── App.test.js
│   │   ├── environment.js
│   │   ├── index.css
│   │   ├── index.js
│   │   ├── logo.svg
│   │   ├── reportWebVitals.js
│   │   └── setupTests.js
│   │
│   ├── package.json
│   └── package-lock.json
│
├── README.md
└── .gitignore
```

---

## ⚙️ Run Project Locally

### Clone the repository

```bash
git clone <your-repo-url>
cd Friend's\ Call
```

### Run Backend

```bash
cd backend
npm install
npm run dev
```

Backend runs on:
- `http://localhost:8000`

### Run Frontend

Open a new terminal:

```bash
cd frontend
npm install
npm start
```

Frontend runs on:
- `http://localhost:3000`

---

## Environment Setup

Create / Update this file:

`frontend/src/environment.js`

```javascript
const server = "http://localhost:8000";
export default server;
```

---

## How to Use

1. Open the app:
   - `http://localhost:3000`
2. Enter your username in the lobby and click **Connect**
3. Join a room by URL:
   - `http://localhost:3000/12345`
4. Share the same room link with your friend to join the same meeting.

---

## Deployment (Render)

### Backend (Render)

- Deploy as **Web Service**
- Start Command:

```bash
npm start
```

- Port: Render uses `process.env.PORT`

### Frontend (Render)

- Deploy as **Static Site**
- Build Command:

```bash
npm run build
```

- Publish Directory:

```bash
build
```

---

## Production Setup (Frontend)

Update frontend environment for production:

`frontend/src/environment.js`

```javascript
const server = "https://YOUR-BACKEND-URL.onrender.com";
export default server;
```

---

## Room Cleanup

- When a user disconnects, they are removed from the room.
- If the room becomes empty, it is deleted from memory.
- Chat messages are also deleted when the room becomes empty.

---

## Author

**Bhavya Goyal**