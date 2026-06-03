# CLAUDE.md

This file gives Claude Code persistent context about this project. Claude reads it automatically at the start of every session — so you don't have to re-explain your stack, conventions, or structure each time.

> **This is an example file.** Copy it into your own project and update each section to match your actual setup.

---

## 🧱 Project overview

**Name:** My Finance Tool  
**What it does:** A web app that allows finance teams to track budget allocations and flag overspend in real time.  
**Status:** In active development — MVP phase

---

## 🛠️ Tech stack

| Layer | Technology |
|---|---|
| Frontend | React + Tailwind CSS |
| Backend | Supabase (database + auth) |
| Deployment | Vercel |
| Version control | GitHub (private repo) |

---

## 📁 Project structure

```
/
├── src/
│   ├── components/       # Reusable UI components
│   ├── pages/            # Page-level components
│   ├── lib/              # Supabase client, utilities
│   └── styles/           # Global styles
├── public/               # Static assets
├── PLAN.md               # Build plan (phase-by-phase)
├── CLAUDE.md             # This file
└── .env.local            # Environment variables (never commit this)
```

---

## ✅ Conventions

- Use **TypeScript** throughout — no plain `.js` files
- Components go in `src/components/`, one file per component
- Use **Tailwind utility classes** for all styling — no custom CSS unless unavoidable
- All Supabase queries go through `src/lib/supabase.ts` — never import the client directly in components
- Keep components small and focused — if a component exceeds ~150 lines, split it

---

## 🔐 Security rules

- Never expose secret keys or tokens in the frontend code
- Always use **Row Level Security (RLS)** in Supabase — every table must have a policy
- All user input must be validated before it hits the database
- `.env.local` is gitignored — never commit environment variables

---

## 🗃️ Database

The main tables are:

- `users` — managed by Supabase Auth
- `budgets` — one row per budget allocation, linked to a user
- `transactions` — individual spend entries, linked to a budget

Foreign keys and RLS policies are set up for all tables. See `PLAN.md` for the full data model.

---

## 🚫 What NOT to do

- Do not install new dependencies without checking with me first
- Do not modify the database schema directly — go through migrations
- Do not refactor working code unless I explicitly ask for it
- Do not add placeholder or mock data to production files

---

## 📌 Current focus

Working on **Phase 2: Budget dashboard** — see `PLAN.md` for details.

Last completed phase: Phase 1 (authentication + user setup) ✅
