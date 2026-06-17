[README.md](https://github.com/user-attachments/files/29041890/README.md)
# 🚀 TaskFlow Pro — NexusFlow

<div align="center">
  <h3>Next-Generation Project Management Platform for Modern Teams</h3>
  <p><em>Inspired by Jira · ClickUp · Asana · Monday.com</em></p>

  ![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=flat-square&logo=node.js&logoColor=white)
  ![Express](https://img.shields.io/badge/Express-4.x-000000?style=flat-square&logo=express&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=flat-square&logo=mongodb&logoColor=white)
  ![Socket.io](https://img.shields.io/badge/Socket.io-4.x-010101?style=flat-square&logo=socket.io&logoColor=white)
  ![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=flat-square&logo=bootstrap&logoColor=white)
  ![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)
  ![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Folder Structure](#-folder-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Deployment](#-deployment)
- [Testing](#-testing)
- [Contributing](#-contributing)
- [Author](#-author)

---

## 📖 About

**NexusFlow** (TaskFlow Pro) is an industry-grade, full-stack project management platform built with Node.js and MongoDB. It brings together task management, real-time collaboration, Kanban boards, sprint planning, team chat, video meetings, AI assistance, and analytics — all in one unified platform.

---

## ✨ Features

### 🔐 Authentication System
- JWT + Refresh Token authentication
- User Registration & Login
- Email Verification workflow
- Forgot / Reset Password
- Update Profile & Upload Avatar
- Secure Bcrypt password hashing

### 🏢 Organization Workspaces
- Create and manage multiple workspaces
- Role-based access control (Super Admin, Admin, Manager, Team Lead, Developer, Tester, Viewer)
- Invite team members by email
- Remove or leave workspaces

### 📁 Project Management
- Create, update, delete, and archive projects
- Project types: Personal, Team, Client
- Priority levels, budgets, and deadlines
- Duplicate and clone project structures

### 🗂️ Kanban Board
- Drag-and-drop between columns (Backlog → Todo → In Progress → Review → Testing → Done)
- Real-time board synchronization via Socket.io
- Quick task creation from the board
- Sprint-filtered views

### 🏃 Sprint Management
- Create and manage Agile sprints
- Start sprint, complete sprint with task rollover
- Team capacity and story point tracking
- Sprint goal definitions

### ✅ Task Management
- Rich task fields: title, description, priority, status, due date, story points, labels, assignee, reporter
- Unlimited subtasks with progress tracking
- Checklists with item-level checkboxes
- File attachments (images, PDF, DOCX, XLSX)
- Task duplication, archival, and deletion
- Work time tracking with start/pause/stop timer

### 💬 Comments System
- Threaded comments with nested replies
- Real-time comment updates

### 🗣️ Team Chat
- Workspace general channel
- Per-project channels
- Direct messages between users
- Real-time typing indicators
- Online/offline user status

### 📹 Video Meeting Integration
- Create and join meeting rooms
- Real-time participant tiles with mic/camera status indicators
- Socket.io-based signaling system

### 📅 Calendar
- Monthly calendar grid view
- Task deadlines plotted on calendar days
- Navigate between months

### 🔔 Notifications
- Bell notification center
- Real-time notification delivery
- Mark individual and all-as-read
- Types: Task Assigned, Comment Added, Project Updated, Meeting Scheduled

### 📖 Activity Logs
- Complete workspace audit trail
- Tracks user, action, entity, and timestamp

### 📂 File Manager
- Upload images, PDFs, Word, and Excel documents
- Attach files to specific tasks or projects
- Download and delete file attachments

### 📊 Dashboard Analytics
- Project, Task, Team, Sprint count metrics
- Task Status Pie Chart (Chart.js)
- Priority Distribution Bar Chart (Chart.js)
- Recent activity feed

### ⏱️ Time Tracking
- Start, Pause, Stop timer per task
- Total time spent tracking (stored in seconds)

### 🕐 Attendance Module
- Clock In / Clock Out
- Work hours auto-calculated
- Attendance history with totals and averages

### 🤖 AI Assistant
- Generate descriptive task templates using AI
- AI-powered priority suggestions
- Estimate completion time from story points
- Sprint planning suggestions (optimal capacity allocation)

### 📚 Knowledge Base (Wiki)
- Create and edit wiki / documentation pages
- Versioned article history
- Full-text search across wiki pages

### 🧑‍💼 Client Portal
- Read-only project delivery progress dashboards
- Progress bars and task completion metrics
- Deadline status indicators

### 📄 Reporting System
- Generate PDF Reports (using PDFKit)
- Generate Excel Reports (using ExcelJS)
- Download and manage report history

### 🔍 Global Search
- Search tasks and wiki pages from any view

### 🌙 Dark Mode
- Dark / Light toggle with persistent localStorage preference

### 📱 Mobile Responsive
- Collapsible sidebar on small screens
- Bootstrap 5 responsive grid throughout

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript (ES Modules), Bootstrap 5, Bootstrap Icons |
| **Charts** | Chart.js 4.x |
| **Real-Time** | Socket.io 4.x |
| **Backend** | Node.js 18+, Express.js 4 |
| **Database** | MongoDB, Mongoose 8 |
| **Authentication** | JWT, Bcryptjs, Refresh Tokens |
| **File Upload** | Multer |
| **PDF Export** | PDFKit |
| **Excel Export** | ExcelJS |
| **Security** | Helmet, CORS, express-rate-limit |
| **Testing** | Mocha, Supertest |
| **Containerisation** | Docker, Docker Compose |

---

## 📁 Folder Structure

```
taskflow-pro/
└── TaskFlow Pro/
    ├── backend/
    │   ├── config/
    │   │   ├── db.js                    # MongoDB connection
    │   │   └── upload.js                # Multer file upload config
    │   ├── controllers/
    │   │   ├── activityController.js
    │   │   ├── aiController.js
    │   │   ├── attendanceController.js
    │   │   ├── authController.js
    │   │   ├── chatController.js
    │   │   ├── fileController.js
    │   │   ├── meetingController.js
    │   │   ├── notificationController.js
    │   │   ├── projectController.js
    │   │   ├── reportController.js
    │   │   ├── sprintController.js
    │   │   ├── taskController.js
    │   │   └── wikiController.js
    │   ├── models/                      # Mongoose data models
    │   ├── routes/                      # Express route definitions
    │   ├── middleware/                  # Auth, error handling middleware
    │   ├── tests/                       # Mocha test suites
    │   └── server.js                    # Express + Socket.io entry point
    ├── frontend/
    │   ├── css/                         # Custom stylesheets
    │   ├── js/                          # Vanilla JS modules
    │   └── index.html                   # App entry point
    ├── .env.example                     # Environment variable template
    ├── .gitignore
    ├── Dockerfile
    ├── docker-compose.yml
    ├── package.json
    └── README.md
```

---

## ✅ Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) v18 or higher
- [npm](https://www.npmjs.com/) v9+
- [MongoDB](https://www.mongodb.com/) (local) or a [MongoDB Atlas](https://www.mongodb.com/atlas) cluster
- [Docker](https://www.docker.com/) *(optional — for containerised setup)*

---

## 🚀 Installation

```bash
# 1. Clone the repository
git clone https://github.com/Dharshan-05/taskflow-pro.git

# 2. Navigate into the project folder
cd "taskflow-pro/TaskFlow Pro"

# 3. Install dependencies
npm install
```

---

## ⚙️ Configuration

Copy the example environment file and fill in your values:

```bash
cp .env.example .env
```

Edit `.env`:

```env
# Server
PORT=5000

# MongoDB connection string
MONGO_URI=mongodb://localhost:27017/nexusflow

# JWT Secret (change this in production!)
JWT_SECRET=your_super_secret_jwt_key
```

---

## ▶️ Running the Application

### Development (with auto-reload)

```bash
npm run dev
```

### Production

```bash
npm start
```

The server will start at **http://localhost:5000**

---

### 🐳 Docker

Run the entire stack (Node.js + MongoDB) with Docker Compose:

```bash
docker-compose up --build
```

Stop containers:

```bash
docker-compose down
```

---

## 📡 API Documentation

The REST API is served from `http://localhost:5000/api`.

| Module | Base Route |
|---|---|
| Auth | `/api/auth` |
| Workspaces | `/api/workspaces` |
| Projects | `/api/projects` |
| Tasks | `/api/tasks` |
| Sprints | `/api/sprints` |
| Chat | `/api/chat` |
| Meetings | `/api/meetings` |
| Notifications | `/api/notifications` |
| Files | `/api/files` |
| Reports | `/api/reports` |
| Wiki | `/api/wiki` |
| Attendance | `/api/attendance` |
| Activity | `/api/activity` |
| AI Assistant | `/api/ai` |

---

## 🧪 Testing

```bash
npm test
```

Tests are located in `backend/tests/` and use **Mocha** + **Supertest**.

---

## 🚢 Deployment

### Option 1 — Docker (recommended)

```bash
docker-compose up -d --build
```

### Option 2 — Manual (e.g., on a VPS / cloud VM)

```bash
# Install PM2 globally
npm install -g pm2

# Start the server
pm2 start backend/server.js --name nexusflow

# Auto-restart on reboot
pm2 startup
pm2 save
```

### Environment checklist before deploying
- [ ] Set `NODE_ENV=production`
- [ ] Use a strong, unique `JWT_SECRET`
- [ ] Point `MONGO_URI` to your production MongoDB Atlas cluster
- [ ] Enable HTTPS (reverse proxy via Nginx or use a cloud load balancer)

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

Please make sure your code passes the test suite (`npm test`) before submitting.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Dharshan-05**  
GitHub: [@Dharshan-05](https://github.com/Dharshan-05)

---

<div align="center">
  <sub>Built with ❤️ · Powered by Node.js + MongoDB + Socket.io</sub>
</div>
