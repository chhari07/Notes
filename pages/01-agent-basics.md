---
title: What is an AI agent
updated: 2026-10-20
---
## Core idea
- **Agent = AI model + tools + a loop**
- It keeps going: think → use a tool → read the result … until the job is done
- Every framework is just a different way to write this same loop

## The one loop
```
User task → Your app (CLI / web / bot) → Agent (model + system prompt)
                                             │
                               needs a tool? ├─ yes → run tool (API, file, DB, search)
                                             │          └─ result goes back to the model (loop)
                                             └─ no  → final answer → user
```

## Remember
- The model only **decides**; your code **runs** the tools
- Loop stops when the model gives a final answer (or a step limit hits)
- Read: Anthropic – *Building effective agents*
