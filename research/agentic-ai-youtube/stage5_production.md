# Stage 5: Building Production Agents (items 16-19): YouTube videos and primary sources

Method: I found candidates with WebSearch and YouTube's own search results page. I checked every video URL below on 2026-10-24 with `https://www.youtube.com/oembed?url=<URL>&format=json`, and all of them returned 200. The titles and channels are copied exactly from the oEmbed response. Durations come from YouTube search listings. Upload dates come from each watch page's `uploadDate` field. I also checked every primary source URL (HTTP 200 on 2026-10-24).

## Which videos explain item 16: A Practical Guide to Building Agents (OpenAI PDF, 2025)?

### Takeaway
OpenAI has not published its own video walkthrough of this PDF. The best match is a deep-dive by the Prompt Engineering channel that came out the week the guide was released. A shorter visual explainer from AI Papers is a good second pick.

### Cited Findings
- Primary source: OpenAI, "A Practical Guide to Building Agents" (PDF, April 2025). Link: https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf. It is built around three parts (model, tools, instructions), when to choose agents over workflows, single-agent vs multi-agent orchestration, and guardrails with human oversight. — [Maginative summary](https://www.maginative.com/article/how-to-build-ai-agents-a-detailed-practical-guide-from-openai/)
- **Video 1 (EXACT MATCH)**
  - URL: https://www.youtube.com/watch?v=oRNblZ-NMSw
  - Title: "Learn How to Build Real-World Agents"
  - Channel: Prompt Engineering
  - Duration / upload: 26:40, uploaded 2025-04-23
  - Note: The video description says it breaks down "OpenAI's latest Agent Blueprint", covering model selection, tool orchestration and deployment tips. — [YouTube](https://www.youtube.com/watch?v=oRNblZ-NMSw); a third-party page also titles it "OpenAI's Blueprint for Production-Ready Agents | Deep Dive" — [Chaindesk](https://chaindesk.ai/ai-news/open-ai-s-blueprint-for-production-ready-agents-deep-dive-oRNblZ-NMSw)
  - Why it's useful: it goes through the OpenAI guide section by section and explains each idea in plain words.
- **Video 2 (EXACT MATCH)**
  - URL: https://www.youtube.com/watch?v=iERasvtdxj0
  - Title: "A practical guide to building agents (feat. OpenAI)"
  - Channel: AI Papers
  - Duration / upload: 8:51, uploaded 2026-07-08
  - Note: The video description says it breaks down OpenAI's guide with chalkboard-style diagrams covering models, tools, instructions, guardrails, orchestration and evaluation loops. — [YouTube](https://www.youtube.com/watch?v=iERasvtdxj0)
  - Why it's useful: a short visual recap, good for quick revision after reading the PDF.

### Inferences
- The guide's ideas are tied to OpenAI's Agents SDK, but they apply to any framework, so its age (2025) does not make these videos outdated.

### Gaps
- I found no official OpenAI-channel video that walks through this PDF. "Intro to Agent Builder" (OpenAI) is a product demo, not the guide, so I left it out.
- AI Papers is a small channel (about 350 views at search time), so its quality is less proven than video 1.

## Which videos explain item 17: 12-Factor Agents (HumanLayer, Dex Horthy, 2025)?

### Takeaway
The author's own AI Engineer talk is the best video. A longer talk by the same author, posted by JumpStars, is a backup.

### Cited Findings
- Primary source: https://github.com/humanlayer/12-factor-agents. The AI Engineer talk page describes production agents as "mostly deterministic software with targeted LLM steps". — [AI Engineer talk page](https://ai.engineer/talks/12-factor-agents)
- **Video 1 (EXACT MATCH, by the author)**
  - URL: https://www.youtube.com/watch?v=8kMaTybvDUw
  - Title: "12-Factor Agents: Patterns of reliable LLM applications — Dex Horthy, HumanLayer"
  - Channel: AI Engineer
  - Duration / upload: 17:06, uploaded 2025-07-03 (about 294K views at search time)
  - Why it's useful: Dex explains the 12 factors himself in 17 minutes. It is the best overview of the repo. — [YouTube](https://www.youtube.com/watch?v=8kMaTybvDUw)
- **Video 2 (EXACT MATCH, by the author, longer version)**
  - URL: https://www.youtube.com/watch?v=Ns1MDpNk6yk
  - Title: "12-factor Agents: Principles of Reliable LLM Application, by Dexter Horthy, Founder, HumanLayer,"
  - Channel: JumpStars
  - Duration / upload: 31:00, uploaded 2025-06-01
  - Why it's useful: a longer version of the same talk, with more time on each factor. — [YouTube](https://www.youtube.com/watch?v=Ns1MDpNk6yk)
- Another recording of the talk (not YouTube) is on the MLOps Community site, from Agents in Production 2025, with a transcript. — [MLOps Community](https://home.mlops.community/public/videos/12-factor-agents-patterns-of-reliable-llm-applications-dexter-horthy-agents-in-production-2025-2025-08-06)

### Inferences
- Video 1 has far more views and comes from the official conference channel, so it should be the main link.

### Gaps
- None significant.

## Which videos explain item 18: Human-in-the-loop (LangGraph interrupts: approve or edit before continuing)?

### Takeaway
LangChain's official video on `interrupt` covers the exact API that the current docs describe: `interrupt()` plus `Command(resume=...)`. CampusX's longer tutorial suits beginners who want to see it coded step by step.

### Cited Findings
- Primary source: https://docs.langchain.com/oss/python/langgraph/interrupts (JS version: https://docs.langchain.com/oss/javascript/langgraph/interrupts). `interrupt` was introduced in December 2024. It pauses the graph, saves state through the persistence layer, and resumes with `graph.invoke(Command(resume=...), thread)`. Use cases include approve/reject, editing state and reviewing tool calls. — [LangChain changelog](https://changelog.langchain.com/announcements/interrupt-simplifying-human-in-the-loop-agents); [LangChain blog](https://blog.langchain.com/making-it-easier-to-build-human-in-the-loop-agents-with-interrupt)
- **Video 1 (EXACT MATCH, official)**
  - URL: https://www.youtube.com/watch?v=6t7YJcEFUIY
  - Title: "LangGraph interrupt: Making it easier to build human-in-the-loop agents"
  - Channel: LangChain
  - Duration / upload: 7:49, uploaded 2024-12-14 (the same day as the blog announcement)
  - Why it's useful: the LangChain team shows how to pause an agent for a human, then resume with approved or edited input. This is still the current API. — [YouTube](https://www.youtube.com/watch?v=6t7YJcEFUIY)
- **Video 2 (EXACT MATCH, beginner tutorial)**
  - URL: https://www.youtube.com/watch?v=xxqZzVZ4gE0
  - Title: "Human in the loop (HITL) using LangGraph | CampusX"
  - Channel: CampusX
  - Duration / upload: 40:04, uploaded 2025-12-12 (about 49K views)
  - Why it's useful: a slow, step-by-step build of an approval flow, good for beginners. — [YouTube](https://www.youtube.com/watch?v=xxqZzVZ4gE0)
- Optional extra (official, newer API layer):
  - URL: https://www.youtube.com/watch?v=SpfT6-YAVPk
  - Title: "Human in the Loop Middleware (Python)"
  - Channel: LangChain
  - Duration / upload: 6:04, uploaded 2025-11-04
  - Why it's useful: it shows the LangChain v1 `create_agent` middleware that adds approve/edit/reject on tool calls, built on top of LangGraph interrupts. — [YouTube](https://www.youtube.com/watch?v=SpfT6-YAVPk)

### Inferences
- Older LangChain videos on "Breakpoints" (Za8CrPqQxpA, 2y old) and "User Feedback" (YmAaKKlDy7k, 2y old) use the earlier `interrupt_before` / `update_state` pattern. I left them out as outdated next to `interrupt()`.

### Gaps
- None significant.

## Which videos explain item 19: Durable execution (LangGraph checkpointing and persistence, so agents resume after a crash)?

### Takeaway
No well-known video covers the "Durable execution" docs page itself. The best choice is CampusX's popular Persistence video, labelled "closest match" because it covers checkpointers, threads and resuming. A short, very new video covers the exact topic but comes from a tiny channel.

### Cited Findings
- Primary sources: https://docs.langchain.com/oss/python/langgraph/durable-execution and https://docs.langchain.com/oss/python/langgraph/persistence. Durable execution needs a checkpointer plus a thread ID. The docs list durability modes ("exit", "async", "sync") and advise deterministic, idempotent steps, with side effects wrapped in tasks. — [LangGraph docs: durable execution](https://docs.langchain.com/oss/python/langgraph/durable-execution)
- **Video 1 (CLOSEST MATCH: persistence and checkpointers)**
  - URL: https://www.youtube.com/watch?v=_IPP7_Bi8uA
  - Title: "Persistence in LangGraph | Time Travel in LangGraph | CampusX"
  - Channel: CampusX
  - Duration / upload: 58:14, uploaded 2025-07-30 (about 105K views)
  - Why it's useful: explains checkpointers, thread IDs, resuming a run and time travel. This is the machinery durable execution is built on. — [YouTube](https://www.youtube.com/watch?v=_IPP7_Bi8uA)
- **Video 2 (EXACT MATCH, small channel)**
  - URL: https://www.youtube.com/watch?v=RsdLmy5_7aw
  - Title: "LangGraph #31: Durable execution – resume after a crash #langgraph #aiagents"
  - Channel: Mehdi Hosseini Moghadam
  - Duration / upload: 5:20, uploaded 2026-09-29 (about 16 views at search time)
  - Note: The description says it builds a multi-step job, makes the email step crash, then resumes from the checkpoint. — [YouTube](https://www.youtube.com/watch?v=RsdLmy5_7aw)
  - Why it's useful: a short demo of exactly what the docs page promises, resuming after a failure. It is very recent, so it matches current APIs.
- Not recommended (outdated): "LangGraph: Persistence" by LangChain (https://www.youtube.com/watch?v=YE6A5d8kNp4, 4:13, uploaded 2024-02-05). It is official but predates the current docs and the durability-mode options.

### Inferences
- For a PDF, pair Video 1 for the concepts with Video 2 for a quick crash-and-resume demo. Readers should still read the durable-execution docs page for the durability modes and the `@task` / idempotency guidance.

### Gaps
- I found no official LangChain video on the "Durable execution" page itself.
- Video 2 is from a very small channel. It is verified live, but its quality is unproven.
