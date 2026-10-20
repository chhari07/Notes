---
title: Prompts
updated: 2026-10-20
---
## A. Building with an AI tool — R G C S R D
1. **Role** – who the AI acts as
2. **Goal** – what you want at the end
3. **Context** – stack, folders, docs
4. **Steps** – "plan first, show me, then code"
5. **Rules** – what NOT to do
6. **Done** – how we know it's finished (tests pass)

## B. Inside the agent's code
```
<role>You are the support agent for Stack.</role>
<goal>Solve it in as few steps as possible.</goal>
<tools>Call get_order BEFORE any order answer.</tools>
<rules>Never invent data. Ask one question if info is missing.</rules>
<output>2-3 short lines + next step</output>
```
- **Tool description** = WHEN to use it + what each input means (model only sees this text)
- **Structured output** = JSON via zod / Pydantic
- **Routing** = small triage prompt picks the agent

## Most used
plan-first · few-shot examples · prompt chaining · "find the cause first" · "list only real bugs"
