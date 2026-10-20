---
title: TypeScript SDKs
updated: 2026-10-20
---
**Setup (all):** Node 20+ → `npm init` → install SDK → API key in `.env` → `src/index.ts`

## Claude Agent SDK
- `npm i @anthropic-ai/claude-agent-sdk`
- `for await (msg of query({ prompt, options }))`
- Options: `model, allowedTools, systemPrompt, permissionMode`
- `CLAUDE.md` = rules · `.claude/agents/` = sub-agents · `.mcp.json` = outside tools
- Built-in tools: Read, Edit, Bash, Grep, WebSearch

## OpenAI Agents SDK
- `npm i @openai/agents zod`
- `new Agent({ name, instructions, tools })` → `await run(agent, input)`
- Triage agent with `handoffs: [a, b]` routes to specialists
- Guardrails + tracing built in

## Vercel AI SDK
- `npm i ai @ai-sdk/google zod`
- `new ToolLoopAgent({ model, instructions, tools, stopWhen })`
- `app/api/chat/route.ts` → `agent.stream()` · UI → `useChat()`
- Change model in one line (google / anthropic / openai / ollama)
