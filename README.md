
# FitSync

> Full-stack fitness tracker that logs meals and workouts with real nutrition data and AI-powered coaching insights.

**Live:** [fitsync-5tf7.onrender.com](https://fitsync-5tf7.onrender.com/login)

#### DEMO : [Demo](https://drive.google.com/file/d/1DETInicyA88unRypztabYwnVn295I3TL/view?usp=sharing)


## Built By

Chimdinma Jason — designed and built end-to-end as my capstone project for the **Meta University Engineering Internship, Summer 2025**. Presented to Meta leadership at end-of-program showcase.

## About

FitSync is a clean, free alternative to paywalled fitness apps. Users log meals (pulled from the Nutritionix API for real nutrition data), log workouts, and track their daily calories in/out with weekly progress charts. An AI chat assistant powered by Gemini provides personalized coaching insights.

## Tech Stack

- **Frontend:** React, Tailwind CSS
- **Backend:** Node.js, Express
- **Database:** PostgreSQL + Prisma
- **Auth:** JWT-secured sessions + Firebase Auth
- **Real-Time:** WebSockets (live workout state sync)
- **APIs:** Nutritionix (food data), Gemini (AI coaching)
- **Deployment:** Render

## Features

- Email/password signup with JWT-secured sessions
- Food search with real nutrition data via the Nutritionix API
- Meal and workout logging with full CRUD
- Daily calories in/out/net summary
- Weekly progress charts
- LLM-generated personalized workout plans
- WebSocket-based live sync (workout state stays consistent across sessions)
- AI chat assistant (Gemini) for personalized coaching

## Local Development

# Backend
```
cd server
npm install
npm run dev
```
# Frontend
```
cd client
npm install
npm run dev
```

Required environment variables (see `.env.example`):
- `DATABASE_URL` (PostgreSQL connection string)
- `NUTRITIONIX_APP_ID` and `NUTRITIONIX_APP_KEY`
- `GEMINI_API_KEY`
- `FIREBASE_*` config keys
- `JWT_SECRET`

## Architecture

React client communicates with Express backend via REST + WebSocket. PostgreSQL stores user data via Prisma ORM. Nutritionix powers food search; Gemini powers the AI assistant. Firebase Auth manages sessions alongside JWT.

