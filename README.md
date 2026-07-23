<div align="center">
  <img src="client/public/logo.svg" alt="SmartResume Logo" width="120" />

  # SmartResume

  **A Modern, AI-Powered Resume Builder built with the MERN Stack**

  <p>
    <a href="https://react.dev/"><img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React 19" /></a>
    <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" /></a>
    <a href="https://expressjs.com/"><img src="https://img.shields.io/badge/Express_5-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" /></a>
    <a href="https://www.mongodb.com/"><img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" /></a>
    <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" /></a>
  </p>
  <p>
    <a href="https://github.com/Vivek9544/SmartResume/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
    <a href="https://github.com/Vivek9544/SmartResume/issues"><img src="https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg" alt="Contributions Welcome"></a>
  </p>
</div>

---

## 🚀 Overview

SmartResume is a full-stack web application designed to help users create professional, ATS-friendly resumes in minutes. By leveraging the power of **Google Gemini AI**, it can enhance professional summaries, rewrite job descriptions with action verbs, and even parse existing PDF resumes to extract structured data. 

Built with a modern UI using React 19 and Tailwind CSS v4, it offers multiple templates, live previews, and secure JWT-based authentication.

## ✨ Features

- 🤖 **AI-Powered Enhancements**: Automatically improve professional summaries and job descriptions using Google Gemini 2.5 Flash.
- 📄 **Resume Parsing**: Upload an existing PDF resume and let the AI extract the data into our structured editor.
- 🎨 **Multiple Templates**: Choose from Classic, Modern, Minimal, and Minimal Image templates with 10 customizable accent colors.
- 🖼️ **Profile Images**: Upload your profile picture with optional automatic background removal (powered by ImageKit).
- 🔒 **Secure Authentication**: JWT-based user registration and login.
- 💾 **Resume Management**: Create, edit, delete, and manage multiple resumes from your personalized dashboard.
- 🖨️ **PDF Export**: Download your finished resume as a perfectly formatted PDF.
- 🔗 **Public Sharing**: Share your resume via a public link.
- 📱 **Responsive Design**: A sleek, dark-themed landing page and a fully responsive dashboard.

## 🏗️ Architecture

### Request Flow
```text
Browser 
   │ (React 19 + Vite + Tailwind v4)
   ▼
Axios Interceptor (Attaches JWT)
   │
   ▼
Express API (Node.js) ──▶ ImageKit (Image CDN & BG Removal)
   │
   ├──▶ Controllers (Auth, Resume, AI)
   │       │
   │       ├──▶ MongoDB (User & Resume Data)
   │       │
   │       └──▶ Google Gemini 2.5 Flash (via OpenAI SDK)
```

## 💻 Tech Stack

| Frontend | Backend | Database & Storage | AI & APIs | Tools |
|----------|---------|--------------------|-----------|-------|
| React 19.1 | Node.js | MongoDB (Mongoose) | Google Gemini 2.5 Flash | Vite 7 |
| Tailwind CSS v4 | Express 5 | ImageKit (Image CDN) | (via OpenAI SDK) | ESLint |
| Redux Toolkit | JWT Auth | | | Multer |
| React Router v7 | bcrypt | | | |
| react-pdftotext | | | | |

## 📁 Folder Structure

```
SmartResume/
├── client/                 # React Frontend
│   ├── public/             # Static assets
│   └── src/
│       ├── app/            # Redux store and slices
│       ├── assets/         # Images and templates
│       ├── components/     # Reusable UI components and forms
│       ├── configs/        # API configuration (Axios)
│       └── pages/          # Application pages (Home, Dashboard, Builder)
│
└── server/                 # Node.js/Express Backend
    ├── configs/            # DB, AI, and ImageKit configs
    ├── controllers/        # Request handlers
    ├── middlewares/        # JWT Auth and file upload middlewares
    ├── models/             # Mongoose schemas
    └── routes/             # API route definitions
```

## 🛠️ Installation & Setup

Follow these steps to set up the project locally.

### Prerequisites
- Node.js (v18+)
- MongoDB (Local or Atlas)
- ImageKit Account
- Google Gemini API Key

### 1. Clone the Repository
```bash
git clone https://github.com/Vivek9544/SmartResume.git
cd SmartResume
```

### 2. Setup the Server (Backend)
```bash
cd server
npm install
```
Create a `.env` file in the `server` directory (use `.env.example` as a template):
```env
PORT=3000
JWT_SECRET=your_super_secret_jwt_key
MONGODB_URI=your_mongodb_connection_string
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
OPENAI_API_KEY=your_gemini_api_key
OPENAI_BASE_URL=https://generativelanguage.googleapis.com/v1beta/openai/
OPENAI_MODEL=gemini-2.5-flash
```
Start the server:
```bash
# For development (uses nodemon)
npm run dev

# For production
npm start
```

### 3. Setup the Client (Frontend)
Open a new terminal window:
```bash
cd client
npm install
```
Create a `.env` file in the `client` directory (use `.env.example` as a template):
```env
VITE_BASE_URL=http://localhost:3000
```
Start the frontend dev server:
```bash
npm run dev
```
The application should now be running at `http://localhost:5173`.

## 📸 Screenshots
*(Coming soon: Add screenshots of the Landing Page, Dashboard, and Resume Builder here)*

## 🔮 Future Improvements

- Add "Forgot Password" and email verification workflows.
- Implement autosave functionality in the resume builder.
- Add drag-and-drop reordering for experience and education sections.
- Enhance client-side form validation (e.g., using Zod or Formik).
- Implement rate limiting for AI endpoints to prevent abuse.

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

Please read our [Contributing Guidelines](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) for details on our code of conduct, and the process for submitting pull requests to us.

## 🛡️ Security

If you discover any security related issues, please refer to our [Security Policy](SECURITY.md).

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 👨‍💻 Author

**Harsha**
- GitHub: [@HARSHATANAKALA](https://github.com/HARSHATANAKALA)

---

