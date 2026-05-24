# QuickBlog — AI-Powered Full-Stack Blog Platform

![MERN](https://img.shields.io/badge/Stack-MERN-green)
![React](https://img.shields.io/badge/Frontend-React-blue)
![Node.js](https://img.shields.io/badge/Backend-Node.js-brightgreen)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-success)
![JWT](https://img.shields.io/badge/Auth-JWT-orange)
![Gemini AI](https://img.shields.io/badge/AI-Google_Gemini-4285F4)
![ImageKit](https://img.shields.io/badge/Media-ImageKit-0F172A)
![Tailwind CSS](https://img.shields.io/badge/UI-TailwindCSS-38B2AC)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Live Demo

Frontend Application  
https://quickblog-opal.vercel.app/

GitHub Repository  
https://github.com/rahulreddy006/QUICKBLOG

---

# Overview

QuickBlog is a modern AI-powered full-stack blogging platform built using the MERN stack architecture.

The platform includes a public blogging interface, an admin dashboard for blog management, AI-generated blog descriptions using Google Gemini, ImageKit-powered media optimization, comment moderation, and a scalable backend API.

This project demonstrates real-world full-stack development practices including REST API development, JWT authentication, cloud media handling, AI integration, database design, frontend-backend integration, deployment, and responsive UI development.

---

# Tech Stack Versions

| Technology | Version |
|---|---|
| Node.js | 18+ Recommended |
| React | 19 |
| Express.js | 5 |
| MongoDB | 9 |
| Vite | 7 |
| Tailwind CSS | 4 |

---

# Architecture

```text
Frontend (React + Vite)
        │
        ▼
Backend API (Express.js)
        │
 ┌──────┼───────────────┐
 ▼      ▼               ▼
MongoDB ImageKit    Gemini AI
                    Content Generation

Admin Dashboard
        │
        ▼
 Blog + Comment Management
```

---

# Features

## Public User Features

- Browse all published blogs
- Search blogs by title or category
- Category filtering
- Read full blog posts
- Comment on blog posts
- Social sharing support
- Newsletter subscription
- Responsive UI across devices

---

## Admin Dashboard Features

- JWT-protected admin authentication
- Dashboard analytics
- Add new blogs
- Rich text editor integration using Quill
- Upload optimized thumbnails using ImageKit
- AI-generated blog descriptions using Gemini
- Publish / unpublish blogs
- Delete blogs
- Moderate comments
- Approve or remove comments

---

# AI Content Generation

QuickBlog integrates Google Gemini AI for intelligent blog content generation.

Workflow:

1. Admin enters blog title
2. Frontend sends request to backend
3. Backend communicates with Gemini API
4. Gemini generates SEO-friendly blog descriptions
5. Generated content is inserted into the editor

---

# Image Optimization Workflow

The application uses ImageKit for cloud-based image optimization.

Workflow:

1. Admin uploads thumbnail
2. Backend processes image upload
3. Image stored on ImageKit
4. Image automatically optimized and compressed
5. Optimized image URL stored in MongoDB
6. Fast-loading images rendered on frontend

---

# Tech Stack

## Frontend

- React 19
- Vite
- React Router DOM
- Axios
- Tailwind CSS v4
- React Hot Toast
- Framer Motion
- Moment.js
- Quill Rich Text Editor
- Marked

---

## Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- Multer
- Google Gemini API
- ImageKit SDK

---

# Folder Structure

```bash
QUICKBLOG/
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── utils/
│   │   └── App.jsx
│
└── README.md
```

---

# Frontend Architecture

## Public Pages

- Home
- Blog Details

---

## Admin Pages

- Dashboard
- Add Blog
- List Blogs
- Comments Moderation
- Admin Login

---

# Backend Architecture

The backend follows a modular Express.js architecture.

## Core Components

### Routes

Responsible for API endpoint definitions and request routing.

### Controllers

Contain blog logic, admin operations, AI generation flow, and comment moderation.

### Middleware

Authentication and file upload handling.

### Models

MongoDB schemas for blogs and comments.

### External Services

- Google Gemini AI
- ImageKit
- MongoDB Atlas

---

# API Endpoints

## Admin

```http
POST /api/admin/login
GET  /api/admin/comments
POST /api/admin/approvecomment
```

---

## Blogs

```http
GET  /api/blog/all
GET  /api/blog/:id
POST /api/blog/add
POST /api/blog/delete
POST /api/blog/togglepublish
POST /api/blog/addcomment
POST /api/blog/generate
```

---

# Environment Variables

Create a `.env` file inside the `backend` directory.

```env
PORT=4000

MONGO_URL=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

GEMINI_API_KEY=your_gemini_api_key

IMAGEKIT_PUBLIC_KEY=your_public_key
IMAGEKIT_PRIVATE_KEY=your_private_key
IMAGEKIT_URL_ENDPOINT=your_url_endpoint
```

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/rahulreddy006/QUICKBLOG.git
```

```bash
cd QUICKBLOG
```

---

# Install Dependencies

## Backend

```bash
cd backend
npm install
```

---

## Frontend

```bash
cd frontend
npm install
```

---

# Running the Project

## Start Backend

```bash
cd backend
npm run server
```

---

## Start Frontend

```bash
cd frontend
npm run dev
```

---

# Deployment

## Frontend Deployment

- Vercel

## Backend Deployment

- Render
- Railway
- VPS Hosting

Note:
The application uses extended serverless function timeout configuration for AI content generation support.

---

# Future Improvements

- Rich markdown editor support
- Blog bookmarking
- User authentication system
- Multi-admin support
- Blog likes and reactions
- Reading time estimation
- AI-generated blog tags
- Dark mode support

---

# Author

Rahul Reddy Kattegummula

GitHub  
https://github.com/rahulreddy006

LinkedIn  
https://www.linkedin.com/in/rahul-reddy-kattegummula

---

# License

This project is licensed under the MIT License.
