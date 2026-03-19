---
name: TrophyHunter Phase 1 Setup
overview: Set up the Next.js project with Tailwind CSS, configure Supabase client, and build the landing page with authentication flow (sign up, login, dashboard).
todos:
  - id: init-nextjs
    content: Initialize Next.js project with TypeScript, Tailwind, App Router
    status: in_progress
  - id: supabase-client
    content: Create Supabase client helpers (browser, server, middleware)
    status: pending
  - id: env-config
    content: Create .env.local.example with Supabase config placeholders
    status: pending
  - id: layout-nav
    content: Build root layout with dark theme and responsive navbar
    status: pending
  - id: landing-page
    content: Build landing page with hero, features, and CTA
    status: pending
  - id: auth-pages
    content: Build login and signup pages with forms
    status: pending
  - id: auth-actions
    content: Implement auth server actions (login, signup, logout)
    status: pending
  - id: dashboard
    content: Build protected dashboard page
    status: pending
  - id: middleware
    content: Add middleware for session refresh and route protection
    status: pending
isProject: false
---

# TrophyHunter Phase 1 — Project Setup and Auth

## Stack

- **Next.js 14+** (App Router) with TypeScript
- **Tailwind CSS** for styling
- **Supabase** for auth, database, and storage
- **@supabase/ssr** for server-side Supabase integration in Next.js

## Steps

### 1. Initialize Next.js Project

- Run `npx create-next-app@latest` with TypeScript + Tailwind + App Router
- Install Supabase dependencies: `@supabase/supabase-js`, `@supabase/ssr`

### 2. Configure Supabase Client

- Create `src/lib/supabase/client.ts` — browser client
- Create `src/lib/supabase/server.ts` — server client (for server components)
- Create `src/lib/supabase/middleware.ts` — session refresh middleware
- Create `.env.local.example` with placeholder Supabase keys

### 3. Build Auth Pages

- `src/app/login/page.tsx` — Login form (email + password)
- `src/app/signup/page.tsx` — Sign up form (email + password + username)
- Auth actions via Supabase Auth (server actions)

### 4. Build Core Pages

- `src/app/page.tsx` — Landing page with hero section, feature highlights, CTA
- `src/app/dashboard/page.tsx` — Protected dashboard (redirect if not logged in)
- Navigation component with auth-aware state

### 5. Middleware for Route Protection

- `src/middleware.ts` — Refresh session + protect `/dashboard` route

### 6. Styling and Layout

- Dark gaming-themed design with Tailwind
- Responsive layout component with navbar
- Modern UI with gradients, cards, and smooth transitions

