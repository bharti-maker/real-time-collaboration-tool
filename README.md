# 📝 Real-Time Text Editor

A simple collaborative text editor where multiple users can type and see each other's changes **live** — built using Node.js and Socket.IO.

> 🎓 This is a student project made to learn real-time web communication basics.

---

## 📁 Folder Structure

```
realtime-editor/
│
├── server.js           ← The backend (runs on Node.js)
│
├── package.json        ← Project info + list of dependencies
│
└── public/             ← All frontend files go here
    ├── index.html      ← The webpage users see
    ├── style.css       ← Styling for the page
    └── app.js          ← Frontend JavaScript (runs in browser)
```

---

## 💡 How It Works — Simple Explanation

```
User A types something
        ↓
Browser sends text to Node.js server (via Socket.IO)
        ↓
Server receives the text and stores it
        ↓
Server sends the text to ALL other connected users
        ↓
User B and User C see the updated text instantly
```

Think of the server as a **relay station** — it receives messages and passes them to everyone else.

---

## 🚀 How to Run the Project

### Step 1: Make sure Node.js is installed
Download it from: https://nodejs.org  
Check if it's installed by running:
```bash
node --version
```

### Step 2: Go into the project folder
```bash
cd realtime-editor
```

### Step 3: Install the required packages
```bash
npm install
```
This reads `package.json` and downloads `express` and `socket.io` into a `node_modules` folder.

### Step 4: Start the server
```bash
node server.js
```
You should see:
```
Server is running at http://localhost:3000
```

### Step 5: Open in browser
Go to: **http://localhost:3000**

### Step 6: Test with multiple users
Open **two browser tabs** (or use two different browsers) at `http://localhost:3000`.  
Start typing in one — you'll see it appear in the other! 🎉

---

## 🔧 Technologies Used

| Technology | What it does |
|------------|-------------|
| **Node.js** | Runs JavaScript on the server |
| **Express** | Serves our HTML/CSS/JS files to the browser |
| **Socket.IO** | Handles real-time, two-way communication |
| **HTML/CSS/JS** | The actual webpage users interact with |

---

## ⚠️ Things This Project Does NOT Have (kept simple on purpose)

- ❌ No login or user accounts
- ❌ No database (text resets when server restarts)
- ❌ No multiple rooms or channels
- ❌ No conflict handling (last writer wins)
- ❌ No mobile-optimized design

These could be added as improvements later!

---

## 📚 What You Can Learn From This

1. How a Node.js + Express server works
2. What WebSockets are and why they're used for real-time apps
3. How Socket.IO makes real-time communication easy
4. How the frontend and backend communicate with events
5. Basic project structure for a web app

---

*Made as a learning project — feel free to modify and experiment!*
