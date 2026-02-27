# 📊 Live Polling System

Welcome to the **Live Polling System**! This is a real-time, interactive polling web application built as part of the SDE Intern Assignment for Intervue.io. 

The platform allows a teacher to create live, time-bound polls and push them to students in real-time. Students can vote, and everyone can watch the results update dynamically as the timer ticks down. I also implemented several bonus features to make the application feel like a complete virtual classroom experience!

## ✨ Features

### Core Requirements Achieved:
- **Real-Time Synchronization:** The server acts as the absolute source of truth. Timers, active polls, and vote counts are flawlessly synced across all connected clients using WebSockets.
- **Role-Based Access:** - **Teachers:** Can create polls (custom questions, options, duration, and marking the correct answer), view participant lists, and end polls.
  - **Students:** Can join using a unique name, wait in a lobby for the next poll, and submit their answers before the timer runs out.
- **Live Results:** Dynamic progress bars update instantly to show how the class voted, highlighting the correct answer and indicating which option the current user chose.

### Bonus / Brownie Points Features Added 🚀:
- **Live Classroom Chat:** A real-time chat popup allowing students and teachers to interact while waiting or discussing results.
- **Kick Participants:** Teachers have the authority to remove (kick) disruptive or inactive students from the session.
- **Poll History:** Teachers can view a history of all past polls and their detailed voting statistics.
- **Tab Isolation:** Robust session management using `sessionStorage` ensures that a single user can test the app in multiple tabs without session overlaps.

---

## 📸 Interface Preview


### 1. Role Selection & Student Join
> Clean and intuitive onboarding for both teachers and students.
![Role Selection Interface](image.png)

### 2. Teacher Dashboard (Create Poll)
> Where the teacher drafts the question, sets the timer, and manages the classroom.
![Teacher Dashboard](image-1.png)

### 3. Student Waiting & Voting View
> The student interface showing the active timer and poll options.
![Student Voting Interface](image-2.png)

### 4. Real-Time Results & Chat
> The post-poll results view alongside the live chat and participant sidebar.
![Results and Chat](image-3.png)

---

## 🛠️ Tech Stack

**Frontend:**
* React.js (with Vite for fast bundling)
* TypeScript
* Tailwind CSS (for modern, responsive styling)
* React Router DOM (for navigation)
* Socket.io-client (for real-time bidirectional communication)

**Backend:**
* Node.js & Express.js
* TypeScript
* Socket.io (for WebSocket implementation)
* MongoDB & Mongoose (for persisting polls, options, and history)

---

## 🚀 Getting Started

Follow these steps to run the project locally on your machine.

### Prerequisites
Make sure you have Node.js and MongoDB installed on your system. 

### 1. Clone the repository
```bash
git clone https://github.com/Gopesh01-hub/Live_Polling_System
cd live_polling_system
```

### 2. Setup the Backend
Open a terminal and navigate to the backend folder:

```bash
cd backend
npm install
```

Create a .env file in the backend directory and add your MongoDB connection string and port:

Code snippet
```bash
PORT=5000
MONGO_URI=mongodb://localhost:27017/live-polling # Or your MongoDB Atlas URI
```

Run the backend server:

```bash
npm run dev
```

### 3. Setup the Frontend
Open a new terminal window and navigate to the frontend folder:

```bash
cd frontend
npm install
npm run dev
```

### 4. Open the App
Navigate to http://localhost:5173 in your browser. Open it in a few different tabs to test out the real-time teacher and student interactions!

### 5. Live Link
[live-polling-system](https://live-polling-system-1-uupb.onrender.com/)
