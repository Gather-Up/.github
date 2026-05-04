# 🎉 Gather-Up

**Gather-Up** is an all-in-one **Event Management & Automation SaaS platform** that streamlines the full lifecycle of an event — from planning and vendor coordination to ticketing, on-site security, parking, and AI-powered insights.

---

## 🌐 Platform Overview

Gather-Up connects four types of users on a single, integrated platform:

| User Type | Role |
|---|---|
| **Event Organizers** | Create and manage events, assign vendors, track analytics |
| **Vendors** | Accept assignments, manage tasks, upload documents, receive payments |
| **Attendees / Customers** | Browse events and purchase tickets |
| **Security Personnel** | Scan tickets on-site, monitor parking, report incidents |

---

## 🏗️ Repositories

### 🖥️ [Gather-Up-Main-Landing-Page](https://github.com/Gather-Up/Gather-Up-Main-Landing-Page)
The marketing landing page and primary web portal for the platform.
- Organizer sign-up / login, vendor portal, and event management dashboard
- AI marketing automation: auto-generate ads, targeted campaigns, performance tracking
- Live dashboard with real-time attendee and event monitoring
- **Stack**: Next.js 16, React 19, TypeScript, Tailwind CSS, MongoDB, JWT

---

### ⚙️ [Gather-Up-Main-Backend](https://github.com/Gather-Up/Gather-Up-Main-Backend)
The core backend service powering the platform's web and mobile applications.
- Secure REST APIs for authentication, data management, and business logic
- Clean architecture with JWT-based auth
- **Stack**: Java, Spring Boot, JWT

---

### 📱 [Gather-Up-Mobile-App](https://github.com/Gather-Up/Gather-Up-Mobile-App)
A React Native mobile application built for **security personnel** working at events.
- QR code ticket scanning with instant validation
- Real-time parking availability checks
- Alerts dashboard for crowd surges, unauthorized entries, and emergencies
- In-field incident reporting with severity, category, and location tagging
- **Stack**: React Native, Expo, Redux/Zustand, Axios

---

### 🔒 [Gather-Up-Security-Backend](https://github.com/Gather-Up/Gather-Up-Security-Backend)
The dedicated backend service for the Security Mobile App.
- **Stack**: Java

---

### 🎟️ [Gather-Up-Ticket-Management-System](https://github.com/Gather-Up/Gather-Up-Ticket-Management-System)
The customer-facing web app where attendees browse events and purchase tickets.
- QR code ticket generation, event listings, checkout flow
- AI-assisted content with Gemini API integration
- **Stack**: Next.js, TypeScript, Gemini API

---

### 🅿️ [Gather-Up-Parking-Management](https://github.com/Gather-Up/Gather-Up-Parking-Management)
A smart parking management system for event venues with automatic license plate recognition.
- Local OCR (Tesseract.js) — no external API costs
- Multi-camera support (IP cameras, DroidCam, USB cameras)
- Real-time slot tracking, fee calculation, and vehicle history
- Socket.IO for live updates across dashboards
- **Stack**: Node.js, Express, React, MongoDB, Tesseract.js, Socket.IO

---

### 🤖 [Gather-Up-AI](https://github.com/Gather-Up/Gather-Up-AI)
A microservices-based AI event planning assistant.
- Natural language event planning via RAG (Retrieval-Augmented Generation)
- Intelligent vendor matching using vector similarity search
- Google Places API integration for venue discovery
- AI image generation for event marketing assets (ComfyUI + Z-Image Turbo + Ollama)
- **Stack**: Python, FastAPI, PyTorch, Sentence Transformers, MongoDB, Ollama, Cloudinary

---

### 🛠️ [Gather-Up-Admin-Console](https://github.com/Gather-Up/Gather-Up-Admin-Console)
The administrative console for managing the platform.
- **Stack**: Next.js, TypeScript, shadcn/ui, Zustand

---

## 🔗 High-Level Architecture

```
                        ┌─────────────────────────┐
                        │   Organizer / Vendor     │
                        │     Landing Page         │
                        │  (Next.js + MongoDB)     │
                        └────────────┬────────────┘
                                     │
               ┌─────────────────────┼──────────────────────┐
               │                     │                      │
   ┌───────────▼──────┐  ┌───────────▼──────┐  ┌──────────▼──────────┐
   │  Main Backend    │  │    AI Service     │  │  Ticket Management  │
   │ (Spring Boot)    │  │ (FastAPI / Python)│  │  System (Next.js)   │
   └───────────┬──────┘  └───────────────────┘  └─────────────────────┘
               │
   ┌───────────┼────────────────────┐
   │           │                    │
┌──▼──────┐  ┌─▼────────────┐  ┌──▼───────────────┐
│ Mobile  │  │   Parking    │  │  Security Backend │
│  App    │  │ Management   │  │     (Java)        │
│(React   │  │ (Node.js +   │  └───────────────────┘
│Native)  │  │  Socket.IO)  │
└─────────┘  └──────────────┘
```

---

## 🛠️ Core Tech Stack Summary

| Layer | Technologies |
|---|---|
| **Web Frontend** | Next.js, React, TypeScript, Tailwind CSS, shadcn/ui |
| **Mobile** | React Native, Expo |
| **Backend (API)** | Spring Boot (Java), FastAPI (Python), Node.js (Express) |
| **Databases** | MongoDB |
| **Auth** | JWT, bcrypt |
| **AI / ML** | PyTorch, Sentence Transformers, Ollama (LLaMA), RAG, ComfyUI |
| **Real-time** | Socket.IO |
| **External APIs** | Google Places API, Cloudinary, Gemini API |
| **DevOps / CI** | GitHub Actions |

---

## 👥 Contributing

Each repository follows a standard fork-and-PR workflow:

1. Fork the relevant repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes and push
4. Open a Pull Request for review

See the individual repository READMEs for setup instructions and environment variable requirements.

---

*Built with ❤️ for event organizers, vendors, and attendees worldwide.*
