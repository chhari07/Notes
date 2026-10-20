---
title: Full app + agent
updated: 2026-10-20
---
The agent is **one part** of your app: its own folder, called through **one API route**.

| Setup | Fits | Like |
|---|---|---|
| **(a)** TS monorepo: `apps/web` + `packages/agents` | Claude / OpenAI / Vercel SDK | — |
| **(b)** Next.js frontend + FastAPI agent backend (SSE) | LangGraph, CrewAI | Mitra AI |
| **(c)** Mobile app + agent API on Vercel | any TS SDK | Stack |

## Flow
```
User → app UI → /api/agent (checks login) → runAgent() → tools (only this user's data)
     ← answer streams back (SSE) ←
```

## 5 rules
1. Model API keys **only on the server** — never in browser or APK
2. Agent code in its own folder → easy to test + swap model
3. App passes the logged-in **user id** to tools — the model never chooses whose data
4. Stream answers (SSE); long jobs → worker / queue
5. Shared types (zod / Pydantic) in one place
