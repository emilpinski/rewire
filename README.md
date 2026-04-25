# Rewire

> Aplikacja produktywności dla osób z ADHD — nawyki, focus timer, AI coach, wspólna praca w rooms.

![Screenshot](./screenshot.png)

## Co to jest

Rewire to PWA (Progressive Web App) zaprojektowana specjalnie dla osób z ADHD. Łączy techniki CBT i terapii skupienia z grywalizacją i wsparciem społecznościowym. Zamiast tradycyjnych list zadań — system "jednej rzeczy", szybkie wygrane (quick wins), timer Pomodoro z AI coachem i rooms do wspólnej pracy w czasie rzeczywistym (body doubling).

Skierowana do dorosłych z ADHD, którzy potrzebują struktury i wsparcia bez przytłaczania interfejsem.

## Funkcje

- **Tryb "jedna rzecz"** — fokus na jednym zadaniu, minimalistyczny UI eliminujący rozproszenia
- **Quick Wins** — lista małych zadań do odbicia w <5 minut dla budowania dopaminy i momentum
- **Focus Timer** — Pomodoro z AI coachem który adaptuje czas do stanu energii użytkownika
- **Rooms (body doubling)** — wspólna praca w czasie rzeczywistym z innymi użytkownikami ADHD
- **Panic Button** — natychmiastowe ćwiczenia oddechowe i linki do helpline przy overwhelm
- **AI Roast** — humorystyczna (ale skuteczna) motywacja od AI coacha
- **Dopamine tracking** — śledzenie dobrego samopoczucia, nagrody, streak heatmap
- **Brain Dump** — szybkie wyrzucenie myśli bez struktury, porządkowanie później
- **Kalendarz** — integracja zadań z widokiem dziennym/tygodniowym
- **Onboarding** — personalizacja do stylu ADHD użytkownika
- **PWA** — działa offline, instalowalna na iOS/Android
- **Supabase Auth** — logowanie email/password lub magic link

## Stack

| Warstwa | Technologia |
|---------|-------------|
| Frontend | Next.js 16, React 19, TypeScript, Tailwind CSS v4 |
| Auth | Supabase Auth (SSR) |
| Baza danych | Supabase (PostgreSQL + RLS) |
| Animacje | Framer Motion |
| OG Images | @vercel/og |
| PWA | Service Worker, Web App Manifest |
| Deploy | Vercel |

## Uruchomienie

```bash
git clone https://github.com/emilpinski/rewire
cd rewire
npm install
cp .env.example .env.local
# Uzupelnij zmienne srodowiskowe
npm run dev
```

## Zmienne środowiskowe

| Zmienna | Opis | Wymagana |
|---------|------|----------|
| `NEXT_PUBLIC_SUPABASE_URL` | URL projektu Supabase | ✅ |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Klucz publiczny Supabase | ✅ |
| `SUPABASE_SERVICE_ROLE_KEY` | Klucz serwisowy (backend) | ✅ |
| `ANTHROPIC_API_KEY` | Klucz Claude AI (coach) | ✅ |
| `NEXT_PUBLIC_APP_URL` | Publiczny URL aplikacji | ✅ |

## Status

WIP — staging

---
Built by [Emil Piński](https://emilpinski.pl)
