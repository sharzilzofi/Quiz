<div align="center">

  <br />

  <p align="center">
    <a href="https://github.com/your-username/your-repo">
      <img src="https://img.shields.io/badge/PROJECT-IN%20DEVELOPMENT-38bdf8?style=for-the-badge&logo=github&logoColor=white" alt="Project Status" />
    </a>
    <img src="https://img.shields.io/badge/NEXT.JS-14-black?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/LICENSE-MIT-8b5cf6?style=for-the-badge" alt="License" />
  </p>

  <h1>Personal Life Dashboard</h1>

  <p>
    <b>One connected system for managing nutrition, finance, workouts, time, daily life, and personal analytics.</b>
  </p>

  <p>
    <a href="#-about-the-product">Explore Project</a> •
    <a href="#-core-modules">Modules</a> •
    <a href="#-getting-started">Run Locally</a> •
    <a href="#-contact--support">Contact</a>
  </p>

  <br />

</div>

---

## 📌 About the Product

> ### *"Track it → Understand it → Improve it"*

### Your life. One dashboard.
**Personal Life Dashboard** is a full-stack web application designed to bring all important areas of everyday life into one connected system.

Instead of using separate applications for food, money, workouts, time tracking, and daily notes, this project brings them together into one personal management platform. The system stores your information and turns it into useful summaries, history, and analytics.

### 🎯 The Vision
The long-term goal is to build a personal operating system where your own data helps you understand how you spend your time, money, energy, and effort.

---

## 🧩 Core Modules

Each section focuses on one part of your life while remaining connected to the overall dashboard:

| Icon | Module | Description |
| :---: | :--- | :--- |
| 🏠 | **Dashboard** | Central overview of your day, statistics, recent activity, and important info. |
| 🍽️ | **Nutrition** | Track food, calories, protein, carbohydrates, fats, fiber, and targets. |
| 💰 | **Finance** | Manage accounts, income, expenses, transfers, balances, and financial history. |
| 🏋️ | **Workout** | Track exercises, sets, reps, weight, volume, workout sessions, and progress. |
| ⏱️ | **Time Tracking** | Track study, work, coding, gym, sleep, entertainment, and free time. |
| 📔 | **Daily Log** | Record sleep, wake time, mood, energy, daily rating, and personal notes. |
| 📊 | **Analytics** | Convert your stored information into charts, trends, and useful statistics. |
| 🕘 | **History** | Search, filter, and review your previous records by date and category. |
| ⚙️ | **Settings** | Manage preferences, targets, integrations, and application data. |

---

## 🔄 Connected System Flow

The modules are designed to work together as a unified system rather than behaving like isolated apps:


┌─────────────┐       ┌─────────────┐       ┌─────────────┐
│ 🍽️ Nutrition │ ────> │  💰 Finance  │ ────> │ 🏋️ Workout  │
└─────────────┘       └─────────────┘       └─────────────┘
│                                           │
▼                                           ▼
┌─────────────┐       ┌─────────────┐       ┌─────────────┐
│   ⏱️ Time   │ ────> │ 📔 Daily Log│ ────> │ 📊 Analytics│
└─────────────┘       └─────────────┘       └─────────────┘

---

## 💻 Technology Stack

Built with a modern full-stack web architecture:

<p align="left">
  <a href="https://nextjs.org"><img src="https://img.shields.io/badge/Next.js%2014-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js 14" /></a>
  <a href="https://react.dev"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" /></a>
  <a href="https://www.typescriptlang.org"><img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /></a>
  <a href="https://tailwindcss.com"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" /></a>
  <a href="https://firebase.google.com"><img src="https://img.shields.io/badge/Firebase_Auth-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase Auth" /></a>
  <a href="https://firebase.google.com"><img src="https://img.shields.io/badge/Cloud_Firestore-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Cloud Firestore" /></a>
  <a href="https://vercel.com"><img src="https://vercel.com"><img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" /></a>
</p>

---

## 🚦 Development Roadmap

### Phase 1 — Foundation (Current)
- [x] **01. Project Setup** — Next.js 14, App Router, TypeScript & Tailwind CSS
- [x] **02. Authentication** — Firebase email/password registration, login, and logout
- [x] **03. Application Shell** — Sidebar, header, navigation & protected application routes
- [x] **04. Firestore Foundation** — Security rules and per-user data isolation

### Upcoming Roadmap
- [ ] 🔥 **Phase 2** — Firestore data layer, settings & user preferences
- [ ] 🍽️ **Phase 3** — Complete nutrition tracking & nutrition analytics
- [ ] 💰 **Phase 4** — Complete finance management & financial analytics
- [ ] 🏋️ **Phase 5** — Workout tracking, timers & progression
- [ ] ⏱️ **Phase 6** — Time tracking, timers & daily timeline
- [ ] 📔 **Phase 7** — Daily log, sleep, mood, energy & notes

---

## ⚡ Getting Started

Run the project locally on your machine in a few quick steps:

### 1. Install dependencies
```bash
npm install

2. Create Firebase project
Create a project on Firebase Console, enable Email/Password Authentication, create a Cloud Firestore Database, and add a Web App to get your config keys.
3. Configure environment variables
Copy the environment example file:
cp .env.example .env.local

Add your Firebase configuration keys to .env.local.
4. Start development server
npm run dev

Then open http://localhost:3000 in your browser.
💬 Contact & Support
Have an app idea or want to create your own personal dashboard, productivity system, or custom web application? Feel free to connect!
<p align="left">
<a href="https://wa.me/YOUR_WHATSAPP_NUMBER" target="_blank">
<img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Contact on WhatsApp" />
</a>
</p>
Sharzil Zofi
Have an idea? Let's build it.
<div align="center">
<sub>© Sharzil Zofi • Personal Life Dashboard — Track it. Understand it. Improve it.</sub>
</div>

