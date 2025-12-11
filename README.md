# 📝 QuickBlog — AI-Powered Full-Stack Blog Application (MERN + Gemini + ImageKit)

QuickBlog is a modern, full-stack, AI-enabled blogging platform built using the **MERN stack**.  
It features **Google Gemini AI integration** for auto-generating blog descriptions, **ImageKit** for optimized media handling, and a complete **Admin Dashboard** for blog + comments management.

### 🔗 Live Demo  
👉 https://quickblog-opal.vercel.app/

### 📦 GitHub Repository  
👉 https://github.com/rahulreddy006/QUICKBLOG

---

## 🚀 Tech Stack

### **Frontend**
- React + Vite  
- Tailwind CSS  
- React Router DOM  
- Axios  
- Moment.js  
- React Hot Toast  
- Framer Motion  
- Quill Rich Text Editor

### **Backend**
- Node.js + Express.js  
- MongoDB + Mongoose  
- Google Gemini API  
- ImageKit  
- JWT Authentication  

### **Deployment**
- Vercel (with extended function timeout to support AI generation)

---

## ⭐ Features

### 👨‍💻 **User Features (Frontend)**
- Browse all blogs  
- Search blogs by title or category  
- Category filtering with smooth animations  
- View full blog details  
- Comment on posts (sent for admin approval)  
- Social media sharing  
- Newsletter subscription  

---

### 🔐 **Admin Dashboard**
- JWT-protected admin login  
- Dashboard with analytics (total blogs, drafts, comments, recent posts)  
- Add Blog
  - Title, subtitle, category  
  - Upload thumbnail (auto-optimized using ImageKit)  
  - Rich text editor with Quill  
  - **AI-generate blog description using Gemini**  
  - Publish toggle  
- Manage Blogs (publish/unpublish/delete)
- Manage Comments (approve/delete)

---

## 🧠 AI Content Generation (Google Gemini)
Admins can click **Generate with AI** → backend sends title → Gemini returns SEO-friendly blog description.

---

## 🖼️ ImageKit Optimization Flow
1. Admin uploads thumbnail  
2. Stored on ImageKit cloud  
3. Auto-transformed to WebP + compressed  
4. Image URL saved in MongoDB  
5. Loads fast on frontend  

---
# 📁 Folder Structure
QUICKBLOG/
│── backend/
│ ├── controllers/
│ ├── routes/
│ ├── models/
│ ├── config/
│ └── server.js
│
└── frontend/
├── src/
│ ├── pages/
│ ├── components/
│ ├── utils/
│ ├── context/
│ └── App.jsx


---

## 🔌 API Endpoints (Important)

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| POST | /api/admin/login | Admin login | ❌ |
| GET | /api/blog/all | All published blogs | ❌ |
| GET | /api/blog/:id | Single blog | ❌ |
| POST | /api/blog/add | Add blog | ✅ Admin |
| POST | /api/blog/delete | Delete blog | ✅ Admin |
| POST | /api/blog/togglepublish | Publish/unpublish | ✅ Admin |
| POST | /api/blog/addcomment | Add comment | ❌ |
| GET | /api/admin/comments | All comments | ✅ Admin |
| POST | /api/admin/approvecomment | Approve comment | ✅ Admin |
| POST | /api/blog/generate | AI description | ✅ Admin |

---

## ⚙️ Installation

```bash
git clone https://github.com/rahulreddy006/QUICKBLOG
cd QUICKBLOG

Backend
cd backend
npm install
npm run dev

Frontend
cd frontend
npm install
npm run dev

🔐 Environment Variables
Backend
MONGO_URL=
JWT_SECRET=
GEMINI_API_KEY=
IMAGEKIT_PUBLIC_KEY=
IMAGEKIT_PRIVATE_KEY=
IMAGEKIT_URL_ENDPOINT=


📄 License
MIT
## 📁 Folder Structure

