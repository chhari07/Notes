---
title: Which framework to pick
updated: 2026-10-20
---
| I want … | Use | Lang |
|---|---|---|
| Claude Code's power (files, bash, edit) in my app | **Claude Agent SDK** | TS + Py |
| Small agents that hand work to each other | **OpenAI Agents SDK** | TS + Py |
| Any model in a web app, switch in 1 line | **Vercel AI SDK** | TS |
| Full control: steps, branches, memory, approval | **LangGraph** | Py (+JS) |
| A quick team of role-based agents in YAML | **CrewAI** | Py |

## Quick rule
- Web app (Next.js) → **Vercel AI SDK**
- Coding / file / ops agent → **Claude Agent SDK**
- Long, stateful, human-in-the-loop → **LangGraph**
- Fast multi-agent demo → **CrewAI**
