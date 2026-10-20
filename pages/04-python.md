---
title: Python frameworks
updated: 2026-10-20
---
**Setup (all):** Python 3.10+ → `uv init` → `uv add <pkg>` → key in `.env` → `uv run main.py`

## Claude Agent SDK
- `uv add claude-agent-sdk`
- `async for msg in query(prompt, ClaudeAgentOptions(allowed_tools, system_prompt))`
- Custom tools: `@tool` + `create_sdk_mcp_server`

## OpenAI Agents SDK
- `uv add openai-agents`
- `Agent(name, instructions, handoffs=[...])` → `Runner.run(triage, msg)`
- `@function_tool` — its **docstring is the tool description**

## LangGraph
- `uv add langgraph langchain`
- `State(TypedDict)` → nodes `call_model / call_tools` → `StateGraph(State)`
- `.add_conditional_edges` (tool call? → tools : END) → `.compile(checkpointer)`
- Most control; can pause for human approval (interrupt)

## CrewAI
- `uv tool install crewai` → `crewai create crew my_crew`
- `agents.yaml` (role, goal, backstory) + `tasks.yaml` (description, expected_output)
- `crewai run` → `kickoff(inputs={...})`
