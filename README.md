# Friend’s Call (WebRTC Video Calling + Chat)

Friend’s Call is a real-time video calling and chat application built using **WebRTC**, **Socket.IO**, **React**, and **Node.js**.  
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