



# 🏆 Captaini - AI-Powered Sports Coaching Marketplace

<div align="center">

<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" />
<img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white" />
<img src="https://img.shields.io/badge/Llama_3.3-0467DF?style=for-the-badge&logo=meta&logoColor=white" />
<img src="https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white" />

<br/><br/>

### A two-sided sports coaching marketplace — AI-matched coaches, seamless booking, verified payments, and auto-generated performance reports, all in one platform.

🌐 **Live Website**: [captaini.vercel.app](https://captaini.vercel.app)  &nbsp;|&nbsp;  
<br/><br/>

https://github.com/user-attachments/assets/71d5a874-8094-4d92-873f-11aaa2ccfeef


<br/>

</div>

---

## 📖 Introduction

**Captaini (كابتني)** is a full-stack web platform that connects trainees with the right sports coach through AI-powered matching. It solves a fragmented, offline market — coaches scattered across social media, manual scheduling via DMs, and no way to objectively compare coaching styles or track progress.

| Typical Coaching Experience | Captaini |
|-----------------------------|----------|
| Coaches scattered across social media & gyms | ✅ Single searchable marketplace across all sports |
| Trainees pick coaches blindly | ✅ AI matching on goals, personality, sport & availability |
| Manual scheduling via chats & calls | ✅ Integrated booking with confirmations & reminders |
| No progress insight | ✅ AI-generated PDF performance reports per trainee |
| Payments handled off-platform | ✅ Paymob, Fawry & Stripe with automatic invoice generation |
| No trust or verification | ✅ ID-based identity verification for coaches and trainees |

---

## ✨ Features

### 🤖 AI Matching Engine
- Pairs trainees with the best-fit coach using goals, sport, personality, coaching style, ratings, location, and availability
- Powered by **Grok** for smart, multi-factor recommendations

### 📅 Integrated Booking System
- Browse coach availability, book, manage, or cancel sessions
- Automated confirmations and reminders via **Google Calendar API** sync
- One platform for discovery, scheduling, and growth

### 📊 AI Performance Reports
- Auto-generated PDF reports per trainee after every session
- Highlights strengths, weaknesses, and progress trends
- Powered by **Llama 3.3** — built from structured coach ratings, no manual input required

### 💳 Verified Payments
- Multi-gateway support: **Paymob**, **Fawry**, and **Stripe**
- Automatic invoice generation and payment verification
- Secure, in-app transactions — no off-platform cash handling

### 🛡️ Identity Verification
- ID-based validation for both coaches and trainees
- Builds a trusted, safe community from day one

### 👥 Community Hub
- Coaches share tips, success stories, and events
- Trainees react, comment, and stay engaged between sessions
- Drives retention through content and social connection

---

## 🚀 Tech Stack

### Frontend
- **React** — Cross-platform web app (coach & trainee) from a single codebase
- **TypeScript** — End-to-end type safety across all components
- **Tailwind CSS v3** — Utility-first styling with `@tailwind` directives
- **Vite** — Fast dev server and build tool with path aliases
- **TanStack Query** — Server-state management and API caching
- **React Hook Form** — Performant form handling and validation

### Backend (`backend-api` — JavaScript)
- **Node.js / Express** — REST API (100% JavaScript), deployed on **MonsterASP.NET** at `captaini-api.runasp.net`
- **Prisma** — Type-safe ORM with schema migrations
- **PostgreSQL (Supabase)** — Cloud-hosted relational database
- **JWT** — Stateless authentication via `Authorization: Bearer` header
- **Postman** — Full API collection in `/postman`

### AI
- **Grok** — AI matching & reasoning engine for coach recommendations
- **Llama 3.3** — AI-powered PDF performance report generation
- **Groq** — Powers the in-app AI assistant (`/api/ai`) for real-time Q&A

### Payments & Scheduling
- **Paymob / Fawry / Stripe** — Multi-gateway payment processing with auto invoice generation
- **Google Calendar API** — Schedule sync and session reminders

### Infrastructure
- **Vercel** — Zero-config frontend deployment
- **MonsterASP.NET** — Backend API hosting
- **Supabase** — PostgreSQL cloud database

---

## 🔄 How It Works

```
Trainee signs up → ID verification
       ↓
Sets goals, sport, personality profile
       ↓
Grok AI matches → Best-fit coach suggested
       ↓
Trainee browses availability → Books a session
       ↓
Payment processed (Paymob / Fawry / Stripe)
       ↓
Session confirmed → Calendar invite + reminder
       ↓
Coach rates trainee → Llama 3.3 generates PDF report
```

---

## 🛣️ API Reference

> **Production API**: `http://captaini-api.runasp.net` · Auth: `Authorization: Bearer <access_token>` (JWT)

### Authentication — `/api/auth`
| Endpoint | Description |
|----------|-------------|
| POST `/register` | Register a new coach or trainee |
| POST `/login` | Authenticate user, return JWT |
| POST `/verify-email` | Verify email address |
| POST `/resend-verification` | Resend verification email |
| POST `/forgot-password` | Initiate password reset |
| POST `/reset-password` | Complete password reset |
| GET  `/me` | Get current authenticated user |

### Profile — `/api/profile`
| Endpoint | Description |
|----------|-------------|
| GET  `/` | Get profile |
| PUT  `/` | Update profile |
| PUT  `/change-password` | Change password |
| POST `/image` | Upload profile image |

### Coaches — `/api/v1/coaches`
| Endpoint | Description |
|----------|-------------|
| GET  `/` | List all coaches with filters |
| GET  `/:id/bookings` | Get coach bookings |
| GET  `/:id/availability` | Get coach availability |
| GET  `/:id/slots` | Get available time slots |

### Bookings — `/api/v1/bookings`
| Endpoint | Description |
|----------|-------------|
| GET  `/` | My bookings |
| GET  `/:id` | Get booking details |
| POST `/` | Create a new booking |

### Session Types — `/api/v1/session-types`
| Endpoint | Description |
|----------|-------------|
| GET  `/` | List session types |
| POST `/` | Create session type |
| PUT  `/:id` | Update session type |
| DELETE `/:id` | Delete session type |

### Payments — `/api/v1/payments`
| Endpoint | Description |
|----------|-------------|
| POST `/` | Initiate payment (Paymob / Fawry / Stripe) |
| GET  `/verify` | Verify payment and confirm booking |

### Reviews — `/api/v1/reviews`
| Endpoint | Description |
|----------|-------------|
| POST `/` | Create a review |
| PUT  `/:id` | Update a review |
| DELETE `/:id` | Delete a review |
| GET  `/` | List reviews |

### Notifications — `/api/notifications`
| Endpoint | Description |
|----------|-------------|
| GET  `/` | List notifications |
| PUT  `/read-all` | Mark all as read |
| PUT  `/preferences` | Update notification preferences |
| POST `/push-subscription` | Register push subscription |

### Files — `/api/files`
| Endpoint | Description |
|----------|-------------|
| POST `/image` | Upload image |
| POST `/video` | Upload video |
| POST `/document` | Upload document |
| GET  `/` | List files |
| GET  `/:id` | Get file |
| DELETE `/:id` | Delete file |

### Admin — `/api/admin`
| Endpoint | Description |
|----------|-------------|
| GET/PUT  `/coach-verification` | Review and approve coach identity verification |
| GET/PUT  `/certification-verification` | Review and approve coach certifications |
| GET/PUT  `/content-moderation` | Moderate community posts and comments |

### AI Assistant — `/api/ai`
| Endpoint | Description |
|----------|-------------|
| POST `/` | AI assistant powered by **Groq** — context-aware Q&A for coaches and trainees |

---

## 🎯 Problem → Solution

| Problem | Our Solution |
|---------|-------------|
| Coaches are fragmented across platforms | Unified multi-sport marketplace |
| No compatibility check before booking | AI matching on personality + goals |
| Manual, chat-based scheduling | Integrated booking with auto-reminders |
| No visibility into trainee progress | AI-generated performance reports |
| Off-platform, untrusted payments | Verified in-app multi-gateway payments |
| No trust or accountability | ID verification for all users |

---

## 📊 SWOT Analysis

| | |
|--|--|
| **Strengths** | AI-driven matching & reports · All-in-one: discovery, booking, payments · Community builds engagement & retention · Verified & trusted coach profiles |
| **Weaknesses** | Cold-start: needs coaches & trainees early · Matching quality depends on data richness · Verification adds onboarding friction · Initial revenue model friction |
| **Opportunities** | Growing fitness & wellness market · Expand into new sports & regions · Corporate wellness partnerships · Untapped Egyptian AI-coaching market |
| **Threats** | Competing apps & social-media coaching · Payment gateway or compliance changes · Coach churn to direct/offline deals · Economic pressure on purchasing power |

---

## 🆚 Competitive Landscape

| Platform | What it does | Gap vs. Captaini |
|----------|-------------|-----------------|
| Trainerize | Coach-client fitness program & messaging tool | No AI matching or multi-sport marketplace |
| CoachUp | Marketplace to search & book sports coaches | No personality-based AI matching or reports |
| MindBody | Booking & scheduling for fitness businesses | Business-first, not coach-trainee matchmaking |
| Thumbtack | General local-service marketplace, incl. coaches | Not sports-specific; no coaching-style matching |

> **Captaini differentiates through AI-powered personality & goal matching, a unified multi-sport marketplace, and automated performance reporting.**

---

## 👥 Team

| Name | GitHub | Role |
|------|--------|------|
| Esraa Mahmoud | [@esraamhmd](https://github.com/esraamhmd) | Frontend |
| Heba | [@Heba205050](https://github.com/Heba205050) | Frontend |
| AMR ELAWADLY | [@Amr-elawadly](https://github.com/Amr-elawadly) | Frontend |
| Youssef Ahmed | [@YoussefAhmed8777](https://github.com/YoussefAhmed8777) | Frontend |
| Mohamed Kamal | [@mokamal11](https://github.com/mokamal11) | Backend |
| alyt2003 | [@alyt2003](https://github.com/alyt2003) | Backend |
| Heba Abd El kreem | [@hebaabdelkreem24](https://github.com/hebaabdelkreem24) | Backend |
| Youssef Ahmed | [@YoussefAhmed2612](https://github.com/YoussefAhmed2612) | AI |
| Youssef Hamed | [@YoussefHamedddd](https://github.com/YoussefHamedddd) | Data Analytics |
| Merola Ashraf | [@Rolaashraf](https://github.com/Rolaashraf) | UI/UX Design |
| Walaa Atallah | [@walaaatallah89](https://github.com/walaaatallah89) | Testing |
| meirhan | [@meirhamlotfy](https://github.com/meirhamlotfy) | Testing |

---

## 📄 License

This project is licensed under the MIT License.

<div align="center">

**Built with ❤️ using React + Node.js + Grok AI**

</div>
