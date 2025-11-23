<div align="center">

# 🚀 Remote Interview Platform

### *A Full-Stack Real-Time Technical Interview Solution*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-19.1-blue.svg)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Latest-green.svg)](https://www.mongodb.com/)

![Demo App](/frontend/public/screenshot-for-readme.png)

*Conduct seamless technical interviews with real-time video calls, collaborative code editing, and automated test validation*

[Features](#-key-features) • [Tech Stack](#-tech-stack) • [Installation](#-installation) • [Usage](#-usage) • [API Documentation](#-api-documentation) • [Contributing](#-contributing)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Installation](#-installation)
- [Environment Setup](#-environment-setup)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [API Documentation](#-api-documentation)
- [Code Execution Engine](#-code-execution-engine)
- [Video & Chat Integration](#-video--chat-integration)
- [Database Schema](#-database-schema)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

**Remote Interview Platform** is a comprehensive, production-ready web application designed to facilitate technical interviews remotely. Built with modern web technologies, it provides a seamless experience for both interviewers and candidates with real-time video communication, collaborative code editing, and instant code execution with automated test validation.

### 🎥 What Makes It Special?

- **Real-Time Collaboration**: Conduct live coding sessions with instant feedback
- **Secure Code Execution**: Run code in isolated environments using Piston API
- **Video Infrastructure**: HD video calls powered by Stream.io with recording capabilities
- **Smart Session Management**: Intelligent room locking, participant tracking, and session persistence
- **Professional UI/UX**: Clean, responsive interface built with React and Tailwind CSS

---

## ✨ Key Features

### 🧑‍💻 **Code Editor**
- **Monaco Editor Integration** - Full VSCode-powered editing experience
- **Multi-Language Support** - JavaScript, Python, and Java with syntax highlighting
- **Real-Time Code Execution** - Instant feedback with test case validation
- **Resizable Panels** - Customizable layout for optimal workflow
- **Code Persistence** - Automatic session state management

### 🎥 **Video & Communication**
- **HD Video Calls** - 1-on-1 video interviews with Stream.io SDK
- **Audio/Video Controls** - Toggle mic and camera with ease
- **Screen Sharing** - Share screens for better collaboration
- **Session Recording** - Record interviews for future review
- **Real-Time Chat** - Integrated messaging system with Stream Chat
- **Participant Management** - Smart room locking (max 2 participants)

### 🔐 **Authentication & Security**
- **Clerk Authentication** - Secure user authentication and management
- **Protected Routes** - Middleware-based route protection
- **Session Isolation** - Each session has unique isolated environments
- **User Profiles** - Comprehensive user data management

### 📊 **Dashboard & Analytics**
- **Live Statistics** - Track active sessions, completions, and participation
- **Session History** - View recent and past interview sessions
- **Active Sessions** - Browse and join ongoing interview rooms
- **User Analytics** - Monitor your interview performance

### 🎯 **Problem Management**
- **Curated Problem Set** - Hand-picked coding challenges
- **Difficulty Levels** - Easy, Medium, and Hard categorization
- **Category Tags** - Array, String, Dynamic Programming, etc.
- **Detailed Descriptions** - Clear problem statements with examples
- **Test Cases** - Comprehensive input/output validation
- **Starter Code** - Pre-written templates for all languages

### ⚙️ **Code Execution Engine**
- **Piston API Integration** - Secure, sandboxed code execution
- **Multi-Language Support** - Execute JavaScript, Python, and Java
- **Test Case Validation** - Automatic comparison with expected outputs
- **Success Feedback** - Confetti animations on successful completion
- **Error Handling** - Clear error messages and runtime feedback

### 🧠 **Background Processing**
- **Inngest Integration** - Async task processing and event-driven workflows
- **Session Cleanup** - Automatic cleanup of completed sessions
- **Webhook Handling** - Process external events efficiently

---

## 🛠️ Tech Stack

### **Frontend**

| Technology | Purpose | Version |
|------------|---------|---------|
| **React** | UI Framework | 19.1.1 |
| **Vite** | Build Tool & Dev Server | 7.1.7 |
| **TailwindCSS** | Utility-First CSS | 4.1.14 |
| **DaisyUI** | Component Library | 5.3.10 |
| **Monaco Editor** | Code Editor | 4.7.0 |
| **Stream.io Video SDK** | Video Call Infrastructure | 1.24.0 |
| **Stream Chat React** | Real-Time Messaging | 13.9.0 |
| **TanStack Query** | Data Fetching & Caching | 5.90.5 |
| **React Router** | Client-Side Routing | 7.9.4 |
| **Clerk React** | Authentication | 5.53.3 |
| **Axios** | HTTP Client | 1.12.2 |
| **Lucide React** | Icon Library | 0.548.0 |
| **Canvas Confetti** | Success Animations | 1.9.3 |
| **React Hot Toast** | Notifications | 2.6.0 |
| **React Resizable Panels** | Layout Management | 3.0.6 |
| **date-fns** | Date Utilities | 4.1.0 |

### **Backend**

| Technology | Purpose | Version |
|------------|---------|---------|
| **Node.js** | Runtime Environment | 18+ |
| **Express** | Web Framework | 5.1.0 |
| **MongoDB** | Database | Latest |
| **Mongoose** | ODM | 8.19.1 |
| **Clerk Express** | Authentication Middleware | 1.7.41 |
| **Stream.io Node SDK** | Video API | 0.7.12 |
| **Stream Chat** | Chat API | 9.24.0 |
| **Inngest** | Background Jobs | 3.44.3 |
| **CORS** | Cross-Origin Resource Sharing | 2.8.5 |
| **dotenv** | Environment Variables | 17.2.3 |

### **External Services**

- **Clerk** - User authentication and management
- **Stream.io** - Video calls and real-time chat
- **MongoDB Atlas** - Cloud database hosting
- **Piston API** - Code execution engine
- **Inngest** - Event-driven workflows
- **Sevalla** - Deployment platform

---

## 🏗️ Architecture

### **System Design**

```
┌─────────────────────────────────────────────────────────────────┐
│                         Client Layer                             │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐          │
│  │   React UI   │  │ Monaco Editor│  │  Stream SDK  │          │
│  └──────────────┘  └──────────────┘  └──────────────┘          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      API Gateway (Express)                       │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐          │
│  │Auth Middleware│ │ CORS Config  │  │Rate Limiting │          │
│  └──────────────┘  └──────────────┘  └──────────────┘          │
└─────────────────────────────────────────────────────────────────┘
                              │
            ┌─────────────────┼─────────────────┐
            ▼                 ▼                  ▼
    ┌───────────────┐ ┌───────────────┐ ┌───────────────┐
    │   Sessions    │ │     Chat      │ │   Inngest     │
    │  Controller   │ │  Controller   │ │   Events      │
    └───────────────┘ └───────────────┘ └───────────────┘
            │                 │                  │
            ▼                 ▼                  ▼
    ┌───────────────────────────────────────────────────┐
    │              MongoDB Database                      │
    │  ┌──────────────┐  ┌──────────────┐              │
    │  │   Sessions   │  │    Users     │              │
    │  └──────────────┘  └──────────────┘              │
    └───────────────────────────────────────────────────┘
                              │
            ┌─────────────────┼─────────────────┐
            ▼                 ▼                  ▼
    ┌───────────────┐ ┌───────────────┐ ┌───────────────┐
    │   Stream.io   │ │     Clerk     │ │  Piston API   │
    │ Video & Chat  │ │     Auth      │ │ Code Executor │
    └───────────────┘ └───────────────┘ └───────────────┘
```

### **Data Flow**

1. **User Authentication**: Clerk handles authentication and provides JWT tokens
2. **Session Creation**: Host creates a session → API generates Stream call ID → DB stores session
3. **Participant Joins**: User joins → API validates → Adds to Stream call → Updates DB
4. **Code Execution**: User submits code → Frontend sends to Piston API → Results validated → UI updated
5. **Real-Time Sync**: All video/chat handled by Stream.io WebSocket connections
6. **Session End**: Host ends → API deletes Stream resources → Updates DB status

---

## 📦 Installation

### **Prerequisites**

Ensure you have the following installed:
- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **MongoDB** (local or Atlas account)
- **Git**

### **Clone Repository**

```bash
git clone https://github.com/Ayush050801/Remote-Interview.git
cd Remote-Interview
```

### **Install Dependencies**

#### Option 1: Install All at Once (Recommended)
```bash
npm run build
```

#### Option 2: Install Separately
```bash
# Backend
cd backend
npm install

# Frontend
cd ../frontend
npm install
```

---

## 🔐 Environment Setup

### **Backend Environment Variables**

Create `backend/.env` file:

```env
# Server Configuration
PORT=3000
NODE_ENV=development
CLIENT_URL=http://localhost:5173

# Database
DB_URL=mongodb://localhost:27017/remote-interview
# Or MongoDB Atlas:
# DB_URL=mongodb+srv://username:password@cluster.mongodb.net/remote-interview

# Clerk Authentication
CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
CLERK_SECRET_KEY=sk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Stream.io (Video & Chat)
STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret

# Inngest (Background Jobs)
INNGEST_EVENT_KEY=your_inngest_event_key
INNGEST_SIGNING_KEY=your_inngest_signing_key
```

### **Frontend Environment Variables**

Create `frontend/.env` file:

```env
# API Configuration
VITE_API_URL=http://localhost:3000/api

# Clerk Authentication
VITE_CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Stream.io
VITE_STREAM_API_KEY=your_stream_api_key
```

### **🔑 Getting API Keys**

#### **Clerk** (Authentication)
1. Go to [clerk.com](https://clerk.com) and sign up
2. Create a new application
3. Navigate to **API Keys** section
4. Copy `Publishable Key` and `Secret Key`

#### **Stream.io** (Video & Chat)
1. Visit [getstream.io](https://getstream.io) and create account
2. Create a new app
3. Go to **Dashboard** → **App Settings**
4. Copy `API Key` and `API Secret`

#### **Inngest** (Background Jobs)
1. Sign up at [inngest.com](https://www.inngest.com)
2. Create a new project
3. Get `Event Key` and `Signing Key` from dashboard

#### **MongoDB** (Database)
1. Use local MongoDB or create free cluster at [mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Get connection string and replace in `DB_URL`

---

## 🚀 Usage

### **Development Mode**

#### **Start Backend Server**
```bash
cd backend
npm run dev
```
Server runs on `http://localhost:3000`

#### **Start Frontend Development Server**
```bash
cd frontend
npm run dev
```
Client runs on `http://localhost:5173`

### **Production Build**

```bash
# Build frontend
cd frontend
npm run build

# Start production server (serves frontend from backend)
cd ../backend
npm start
```

### **Application Workflow**

1. **Sign Up/Login** → Navigate to homepage and authenticate via Clerk
2. **Dashboard** → View statistics, active sessions, and recent history
3. **Create Session** → Click "Create Session", select problem and difficulty
4. **Join Session** → Browse active sessions and join as participant
5. **Conduct Interview**:
   - Video call automatically connects
   - Use chat for communication
   - Write code in Monaco editor
   - Execute code with "Run Code" button
   - Test against predefined test cases
6. **End Session** → Host clicks "End Session" to complete

---

## 📁 Project Structure

```
Remote-Interview/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── chatController.js       # Chat message handling
│   │   │   └── sessionController.js     # Session CRUD operations
│   │   ├── lib/
│   │   │   ├── db.js                   # MongoDB connection
│   │   │   ├── env.js                  # Environment config validator
│   │   │   ├── inngest.js              # Background job definitions
│   │   │   └── stream.js               # Stream.io client initialization
│   │   ├── middleware/
│   │   │   └── protectRoute.js         # Auth middleware
│   │   ├── models/
│   │   │   ├── Session.js              # Session schema
│   │   │   └── User.js                 # User schema
│   │   ├── routes/
│   │   │   ├── chatRoutes.js           # Chat endpoints
│   │   │   └── sessionRoute.js         # Session endpoints
│   │   └── server.js                   # Express app entry point
│   ├── .env.example                    # Environment template
│   └── package.json                    # Backend dependencies
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   │   └── sessions.js             # API client functions
│   │   ├── components/
│   │   │   ├── ActiveSessions.jsx      # Active session list
│   │   │   ├── CodeEditorPanel.jsx     # Monaco editor component
│   │   │   ├── CreateSessionModal.jsx  # Session creation modal
│   │   │   ├── Navbar.jsx              # Navigation bar
│   │   │   ├── OutputPanel.jsx         # Code execution output
│   │   │   ├── ProblemDescription.jsx  # Problem display
│   │   │   ├── RecentSessions.jsx      # Session history
│   │   │   ├── StatsCards.jsx          # Dashboard statistics
│   │   │   ├── VideoCallUI.jsx         # Stream video integration
│   │   │   └── WelcomeSection.jsx      # Landing page hero
│   │   ├── data/
│   │   │   └── problems.js             # Coding problems dataset
│   │   ├── hooks/
│   │   │   ├── useSessions.js          # Session data hooks
│   │   │   └── useStreamClient.js      # Stream.io hooks
│   │   ├── lib/
│   │   │   ├── axios.js                # Axios instance config
│   │   │   ├── piston.js               # Code execution client
│   │   │   ├── stream.js               # Stream client setup
│   │   │   └── utils.js                # Utility functions
│   │   ├── pages/
│   │   │   ├── DashboardPage.jsx       # Main dashboard
│   │   │   ├── HomePage.jsx            # Landing/login page
│   │   │   ├── ProblemPage.jsx         # Solo practice mode
│   │   │   ├── ProblemsPage.jsx        # Problem listing
│   │   │   └── SessionPage.jsx         # Active interview room
│   │   ├── App.jsx                     # Root component & routing
│   │   ├── index.css                   # Global styles
│   │   └── main.jsx                    # React entry point
│   ├── public/                         # Static assets
│   ├── .env.example                    # Environment template
│   ├── index.html                      # HTML template
│   ├── vite.config.js                  # Vite configuration
│   └── package.json                    # Frontend dependencies
│
├── package.json                        # Root package file
└── README.md                           # This file
```

---

## 🔌 API Documentation

### **Base URL**
```
http://localhost:3000/api
```

### **Authentication**
All protected routes require Clerk authentication token in headers:
```
Authorization: Bearer <clerk_token>
```

---

### **Session Endpoints**

#### **Create Session**
```http
POST /api/sessions/create
```

**Request Body:**
```json
{
  "problem": "two-sum",
  "difficulty": "easy"
}
```

**Response:**
```json
{
  "session": {
    "_id": "session_id",
    "problem": "two-sum",
    "difficulty": "easy",
    "host": "user_id",
    "participant": null,
    "status": "active",
    "callId": "session_timestamp_random",
    "createdAt": "2025-11-23T10:00:00.000Z"
  }
}
```

---

#### **Get Active Sessions**
```http
GET /api/sessions/active
```

**Response:**
```json
{
  "sessions": [
    {
      "_id": "session_id",
      "problem": "two-sum",
      "difficulty": "easy",
      "host": {
        "_id": "user_id",
        "name": "John Doe",
        "email": "john@example.com",
        "profileImage": "url",
        "clerkId": "clerk_id"
      },
      "participant": null,
      "status": "active",
      "callId": "call_id"
    }
  ]
}
```

---

#### **Get Recent Sessions**
```http
GET /api/sessions/recent
```

**Response:** Returns completed sessions where user was host or participant

---

#### **Get Session by ID**
```http
GET /api/sessions/:id
```

**Response:**
```json
{
  "session": {
    "_id": "session_id",
    "problem": "two-sum",
    "difficulty": "easy",
    "host": { "name": "John", ... },
    "participant": { "name": "Jane", ... },
    "status": "active",
    "callId": "call_id"
  }
}
```

---

#### **Join Session**
```http
POST /api/sessions/join/:id
```

**Response:**
```json
{
  "session": {
    "_id": "session_id",
    "participant": "user_id",
    ...
  }
}
```

**Constraints:**
- Session must be active
- Cannot have more than 2 participants
- Host cannot join as participant

---

#### **End Session**
```http
POST /api/sessions/end/:id
```

**Response:**
```json
{
  "session": { ... },
  "message": "Session ended successfully"
}
```

**Constraints:**
- Only host can end session
- Deletes Stream call and chat channel

---

### **Chat Endpoints**

#### **Get Chat Token**
```http
GET /api/chat/token
```

**Response:**
```json
{
  "token": "stream_chat_token",
  "userId": "clerk_user_id"
}
```

---

### **Health Check**

```http
GET /health
```

**Response:**
```json
{
  "msg": "api is up and running"
}
```

---

## ⚙️ Code Execution Engine

### **Piston API Integration**

The platform uses [Piston API](https://github.com/engineer-man/piston) for secure code execution:

**Supported Languages:**
- JavaScript (Node.js 18)
- Python (3.10+)
- Java (JDK 15+)

**Execution Flow:**
```javascript
// frontend/src/lib/piston.js
const executeCode = async (language, code) => {
  const response = await axios.post('https://emkc.org/api/v2/piston/execute', {
    language: language,
    version: '*',
    files: [{
      content: code
    }]
  });
  return response.data;
};
```

**Test Case Validation:**
```javascript
const validateOutput = (actualOutput, expectedOutput) => {
  // Normalize whitespace and newlines
  const normalize = (str) => str.trim().replace(/\s+/g, ' ');
  return normalize(actualOutput) === normalize(expectedOutput);
};
```

---

## 🎥 Video & Chat Integration

### **Stream.io Configuration**

**Backend Initialization:**
```javascript
// backend/src/lib/stream.js
import { StreamClient } from '@stream-io/node-sdk';
import { StreamChat } from 'stream-chat';

export const streamClient = new StreamClient(
  process.env.STREAM_API_KEY,
  process.env.STREAM_API_SECRET
);

export const chatClient = StreamChat.getInstance(
  process.env.STREAM_API_KEY,
  process.env.STREAM_API_SECRET
);
```

**Frontend Setup:**
```javascript
// frontend/src/lib/stream.js
import { StreamVideoClient } from '@stream-io/video-react-sdk';

const client = new StreamVideoClient({
  apiKey: import.meta.env.VITE_STREAM_API_KEY,
  user: {
    id: userId,
    name: userName,
    image: profileImage
  },
  token: userToken
});
```

**Features Enabled:**
- HD video calls (up to 1080p)
- Screen sharing
- Call recording
- Audio/video device controls
- Real-time chat messaging
- Participant management

---

## 💾 Database Schema

### **User Model**
```javascript
{
  clerkId: String (unique, required),
  name: String (required),
  email: String (unique, required),
  profileImage: String,
  createdAt: Date,
  updatedAt: Date
}
```

### **Session Model**
```javascript
{
  problem: String (required),
  difficulty: Enum ['easy', 'medium', 'hard'] (required),
  host: ObjectId → User (required),
  participant: ObjectId → User (nullable),
  status: Enum ['active', 'completed'] (default: 'active'),
  callId: String (unique),
  createdAt: Date,
  updatedAt: Date
}
```

### **Indexes**
```javascript
// Optimize queries
Session.index({ status: 1, createdAt: -1 });
Session.index({ host: 1, status: 1 });
Session.index({ participant: 1, status: 1 });
User.index({ clerkId: 1 });
User.index({ email: 1 });
```

---

## 🌐 Deployment

### **Backend Deployment (Sevalla/Railway/Heroku)**

1. **Set Environment Variables** on hosting platform
2. **Configure Build Command:**
   ```bash
   npm install --prefix backend
   ```
3. **Configure Start Command:**
   ```bash
   npm start --prefix backend
   ```

### **Full-Stack Deployment**

1. **Build Frontend:**
   ```bash
   npm run build
   ```
2. **Deploy Backend** with frontend build served statically
3. **Environment Variables:** Set all production keys
4. **Database:** Use MongoDB Atlas for production

### **Environment Considerations**

- Set `NODE_ENV=production`
- Use production database URL
- Enable CORS for production domain
- Set `CLIENT_URL` to production frontend URL
- Secure all API keys

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository**
2. **Create feature branch:**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit changes:**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to branch:**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open Pull Request**

### **Code Standards**
- Follow existing code style
- Write clear commit messages
- Add comments for complex logic
- Test thoroughly before submitting

---

## 📝 License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Ayush Singh**

- GitHub: [@Ayush050801](https://github.com/Ayush050801)
- Email: ayush@example.com

---

## 🙏 Acknowledgments

- **Clerk** - Authentication infrastructure
- **Stream.io** - Video and chat SDKs
- **Piston** - Code execution engine
- **MongoDB** - Database platform
- **Inngest** - Background job processing
- **Vercel** - Inspiration for UI/UX patterns

---

## 📚 Additional Resources

- [Clerk Documentation](https://clerk.com/docs)
- [Stream.io Video SDK](https://getstream.io/video/docs/)
- [Stream Chat SDK](https://getstream.io/chat/docs/)
- [Piston API](https://github.com/engineer-man/piston)
- [Monaco Editor](https://microsoft.github.io/monaco-editor/)
- [TanStack Query](https://tanstack.com/query/latest)

---

<div align="center">

### ⭐ If you find this project helpful, please give it a star!

**Made with ❤️ by Ayush Singh**

</div>
