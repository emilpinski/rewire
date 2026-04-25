# Rewire

> Productivity app for people with ADHD — habits, focus timer, AI coach, collaborative work rooms.

![Screenshot](./screenshot.png)

## What is it

Rewire is a PWA (Progressive Web App) designed specifically for people with ADHD. It combines CBT and focus therapy techniques with gamification and social support. Instead of traditional to-do lists — a "one thing" system, quick wins, a Pomodoro timer with an AI coach, and real-time collaborative work rooms (body doubling).

Built for adults with ADHD who need structure and support without an overwhelming interface.

## Features

- **"One thing" mode** — focus on a single task, minimalist UI eliminating distractions
- **Quick Wins** — list of small tasks completable in <5 minutes for building dopamine and momentum
- **Focus Timer** — Pomodoro with an AI coach that adapts time to the user's energy level
- **Rooms (body doubling)** — real-time collaborative work with other ADHD users
- **Panic Button** — immediate breathing exercises and helpline links when overwhelmed
- **AI Roast** — humorous (but effective) motivation from the AI coach
- **Dopamine tracking** — wellbeing tracking, rewards, streak heatmap
- **Brain Dump** — quick thought offloading without structure, organize later
- **Calendar** — task integration with daily/weekly view
- **Onboarding** — personalization to the user's ADHD style
- **PWA** — works offline, installable on iOS/Android
- **Supabase Auth** — email/password or magic link login

## Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Next.js 16, React 19, TypeScript, Tailwind CSS v4 |
| Auth | Supabase Auth (SSR) |
| Database | Supabase (PostgreSQL + RLS) |
| Animations | Framer Motion |
| OG Images | @vercel/og |
| PWA | Service Worker, Web App Manifest |
| Deploy | Vercel |

## Getting Started

```bash
git clone https://github.com/emilpinski/rewire
cd rewire
npm install
cp .env.example .env.local
# Fill in environment variables
npm run dev
```

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_SUPABASE_URL` | Supabase project URL | ✅ |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Supabase public key | ✅ |
| `SUPABASE_SERVICE_ROLE_KEY` | Supabase service key (backend) | ✅ |
| `OPENROUTER_API_KEY` | OpenRouter API key (coach) | ✅ |
| `NEXT_PUBLIC_APP_URL` | Public application URL | ✅ |

## Status

WIP — staging

---
Built by [Emil Piński](https://emilpinski.pl)
