# 🚀 Codelytic EduTech Software — Official Website

> **Innovating Education** — Empowering the next generation of engineers, designers, and innovators with high-impact tech training and personalized 1-on-1 industry mentorship.

![Codelytic Preview](codelytic-logo.jpg)

---

## 🌐 Live Website
- **GitHub Pages:** [https://official-codelytic.github.io/Codelytic-EduTech-Software-Website/](https://official-codelytic.github.io/Codelytic-EduTech-Software-Website/)
- **Repository:** [https://github.com/official-codelytic/Codelytic-EduTech-Software-Website](https://github.com/official-codelytic/Codelytic-EduTech-Software-Website)

---

## ✨ Features

### 🔐 1. Real Google Authentication (Firebase Auth)
- Direct integration with **Google OAuth 2.0** via **Firebase Authentication**.
- Account selection prompt (`prompt: 'select_account'`) allowing users to choose or switch Google accounts.
- Automatic extraction of user display name, email, and Google profile photo.
- Fallback initials avatar generator when profile photos are unavailable.
- Session persistence (`LOCAL`) maintaining user login state across page reloads.

### 🎓 2. Interactive Course Enrollment
- 4 comprehensive curriculum tracks:
  1. **Full Stack Engineering** (MERN, Next.js, Microservices & Cloud)
  2. **Artificial Intelligence & Data Science** (Python, Machine Learning, Deep Learning)
  3. **Prompt Engineering & Generative AI** (LLMs, AI Agents, Production Workflows)
  4. **UI/UX Design & Product Strategy** (Figma, Design Systems, Usability Testing)
- Live enrollment modal with course pre-selection.
- Dynamic enrolled status tracking (`✅ Enrolled` badge) saved in `localStorage`.

### 📬 3. Automated Dual-Channel Email System
- **Company Notifications:** Instant enrollment alert delivered directly to `official.codelytic@gmail.com`.
- **Student Confirmations:** Personalized confirmation receipt sent to the student's email address with Enrollment ID and curriculum details.
- Integrated with FormSubmit AJAX endpoint and local Express API fallback.

### 👤 4. Personalized Learner Profile
- Interactive profile modal featuring:
  - Official Codelytic company branding.
  - Authenticated user's Google profile picture and verified email.
  - Unique Student Learner ID (e.g., `#CDL-2026-XXXX`).
  - Active scholar status badge.
  - One-click account switcher and secure logout.

### 📱 5. Modern Responsive UI / UX
- Built with **Tailwind CSS** and **Google Material Symbols**.
- Fully responsive across mobile, tablet, laptop, and 4K displays.
- Smooth scroll navigation with dynamic active section spy.
- Animated micro-interactions, smooth modals, and glassmorphic navigation header.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | HTML5, JavaScript (ES6+), Tailwind CSS, Plus Jakarta Sans |
| **Authentication** | Firebase Authentication (v10 compat) — Google OAuth Provider |
| **Icons & Design** | Google Material Symbols Outlined, SVG Icons |
| **Form Handling** | FormSubmit AJAX API, EmailJS Browser SDK |
| **Local Backend** | Node.js, Express.js (Enrollment & Inquiry API) |
| **Hosting** | GitHub Pages |

---

## 📂 Project Structure

```text
Codelytic-EduTech-Software-Website/
├── index.html           # Main entry point (served by GitHub Pages)
├── code.html            # Core website source code
├── activate.html        # Form activation verification page
├── codelytic-logo.jpg   # Official brand logo
├── DESIGN.md            # Design system, color tokens & typography specs
├── enrollments.json     # Local database of student enrollments
├── inquiries.json       # Local database of student contact inquiries
└── README.md            # Documentation & project overview
```

---

## 🚀 Getting Started Locally

### Prerequisites
- [Node.js](https://nodejs.org/) (v16.0 or higher recommended)
- A modern web browser (Google Chrome, Microsoft Edge, etc.)

### 1. Clone the Repository
```bash
git clone https://github.com/official-codelytic/Codelytic-EduTech-Software-Website.git
cd Codelytic-EduTech-Software-Website
```

### 2. Run with Local Server
Because Google OAuth requires an `http://` or `https://` origin, run a local web server rather than opening `index.html` as a file:

```bash
# Using Node.js http-server or npx
npx serve -l 3000 .
```

Then open your browser and navigate to:
```
http://localhost:3000/
```

---

## ⚙️ Firebase Authentication Setup

To use your own Firebase project for authentication:

1. Create a project at [Firebase Console](https://console.firebase.google.com/).
2. Enable **Authentication** $\rightarrow$ **Sign-in method** $\rightarrow$ **Google** $\rightarrow$ Click **Enable** and configure your support email.
3. Under **Authentication** $\rightarrow$ **Settings** $\rightarrow$ **Authorized domains**, add:
   - `localhost`
   - `officialcodelytic.github.io`
   - `official-codelytic.github.io`
4. Copy your web app config and update `firebaseConfig` in `index.html`:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.firebasestorage.app",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

---

## 📞 Contact & Support

- **Organization:** Codelytic EduTech Software
- **Email:** [official.codelytic@gmail.com](mailto:official.codelytic@gmail.com)
- **GitHub:** [@official-codelytic](https://github.com/official-codelytic)
- **Tagline:** *Innovating Education — Building World-Class Engineers.*

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
