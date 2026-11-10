# Stages 6-7: Multi-agent systems and coding agents (items 20-25): best YouTube videos

How I verified (2026-10-24): every video URL below returned HTTP 200 from `https://www.youtube.com/oembed?url=<URL>&format=json`. Title and channel are copied exactly from the oEmbed response. Duration and upload date come from the video's watch page (`lengthSeconds`, `uploadDate`). Every primary-source URL returned HTTP 200 too. I did not invent or guess any video IDs. Each one came from a live YouTube search results page and was then checked with oEmbed.

## Which videos explain each item, and how well?

### Takeaway
Items 21 (Anthropic) and 23 (MetaGPT) have no talk by the authors. For those, the best choices are explainers that walk through the original post or paper. Item 20 (Handoffs) has a good handoffs-only tutorial from a third party. Items 22, 24 and 25 have talks by the authors themselves: Chi Wang and Victor Dibia for AutoGen, John Yang for SWE-bench, and Ofir Press for SWE-agent.

### Cited Findings

#### 20. Handoffs (OpenAI Agents SDK docs)
Primary source: https://openai.github.io/openai-agents-python/handoffs/

- Video 1: https://www.youtube.com/watch?v=LuarehusOWU
  - Title: "OpenAI Agents SDK Handoffs | Deep Dive Tutorial" | Channel: James Briggs | 34:50 | Uploaded 2025-05-17
  - Note: Covers only handoffs. It compares them with the "agents-as-tools" pattern and builds a working multi-agent example in Python. — [YouTube](https://www.youtube.com/watch?v=LuarehusOWU)
  - Match: EXACT
- Video 2: https://www.youtube.com/watch?v=35nxORG1mtg
  - Title: "Agents SDK from OpenAI! | Full Tutorial" | Channel: James Briggs | 22:24 | Uploaded 2025-03-12
  - Note: A beginner tour of the whole SDK (agent loop, tools, handoffs, guardrails), released just after launch. Watch it before Video 1. — [YouTube](https://www.youtube.com/watch?v=35nxORG1mtg)
  - Match: Closest match. It covers the whole SDK, and handoffs are one part.
- Optional, official but newer: https://www.youtube.com/watch?v=tK32trvj_b4
  - Title: "Build Hour: Agents SDK" | Channel: OpenAI | 47:40 | Uploaded 2026-05-28
  - Note: OpenAI's own session on the updated SDK, focused on long-running agents and a "model-native harness". The description does not mention handoffs. — [YouTube](https://www.youtube.com/watch?v=tK32trvj_b4)
  - Match: Closest match (official SDK video, not handoffs-specific).
- TypeScript alternative: https://www.youtube.com/watch?v=AF5BBIj3N-Q, "Agent Handoffs | OpenAI Agent SDK with Typescript", Piyush Garg, 18:08, 2025-11-11. Match: EXACT, but it uses the TypeScript SDK. — [YouTube](https://www.youtube.com/watch?v=AF5BBIj3N-Q)
- Outdated note: the James Briggs videos are from the 2025 launch-era API. The 2026 OpenAI Build Hour describes an "updated Agents SDK", so some code may differ from the current docs.

#### 21. How we built our multi-agent research system (Anthropic, June 2025)
Primary source: https://www.anthropic.com/engineering/multi-agent-research-system. It now redirects to https://www.anthropic.com/research/multi-agent-research-system, and both URLs work. — [Anthropic](https://www.anthropic.com/engineering/multi-agent-research-system)

- Video 1: https://www.youtube.com/watch?v=0HljLKVdtjo
  - Title: "Anthropic: How to Build Multi Agent Systems" | Channel: Alejandro AO | 37:33 | Uploaded 2025-06-19
  - Note: Walks through Anthropic's article (the description links it): the lead agent, parallel subagents and prompting tips, then advice for building your own. — [YouTube](https://www.youtube.com/watch?v=0HljLKVdtjo)
  - Match: EXACT (third-party walkthrough of the post)
- Video 2: https://www.youtube.com/watch?v=IPu3HwtQb18
  - Title: "How Anthropic Builds Multi-Agent Systems: Patterns and Pitfalls" | Channel: Databricks Events | 17:55 | Uploaded 2026-08-25
  - Note: Talk by Anthropic's principal architect for strategic accounts. The main point is to perfect a single agent first and only then add multi-agent setups. It pairs well with the blog post's tradeoffs. — [YouTube](https://www.youtube.com/watch?v=IPu3HwtQb18)
  - Match: Closest match. The speaker is from Anthropic and the topic is the same, but the description does not say whether the talk covers the Research feature itself.
- Optional, very short official product demo: https://www.youtube.com/watch?v=R-KJgjIrh24, "Getting started with research in Claude.ai", Anthropic, 2:50, 2025-12-02. It shows the Research feature from the user's side, not how it was built. Match: Closest match. — [YouTube](https://www.youtube.com/watch?v=R-KJgjIrh24)

#### 22. AutoGen (Wu et al., 2023, arXiv 2308.08155, Microsoft)
Primary source: https://arxiv.org/abs/2308.08155 (code: https://github.com/microsoft/autogen)

- Video 1: https://www.youtube.com/watch?v=MCYzYzaWChY
  - Title: "AutoGen: A Multi-Agent AI Framework - Victor Dibia & Chi Wang, Microsoft" | Channel: The Linux Foundation | 33:11 | Uploaded 2023-12-18
  - Note: Talk by the authors on AutoGen's core ideas: agents you can talk to, conversation patterns, and humans in the loop. It is the closest thing to a talk version of the paper. — [YouTube](https://www.youtube.com/watch?v=MCYzYzaWChY)
  - Match: EXACT (authors' talk)
- Video 2: https://www.youtube.com/watch?v=2RT8i-VP7V0
  - Title: "AutoGen: Enabling Next Gen LLM Applications via Multi Agent Conversation Framework" | Channel: Data Science Gems | 26:00 | Uploaded 2023-09-30
  - Note: Goes through the paper section by section (the title is the paper's title), which is useful for reading along. — [YouTube](https://www.youtube.com/watch?v=2RT8i-VP7V0)
  - Match: EXACT (paper explainer)
- Optional short official updates from the Microsoft Research channel:
  - https://www.youtube.com/watch?v=j_mtwQiaLGU, "What's new in AutoGen? | Microsoft Research Forum", Microsoft Research, 5:06, 2024-03-11 (Chi Wang). — [YouTube](https://www.youtube.com/watch?v=j_mtwQiaLGU)
  - https://www.youtube.com/watch?v=LM6JcqLeF0U, "AutoGen v0.4: Reimagining the foundation of agentic AI for scale and more | Microsoft Research Forum", Microsoft Research, 8:06, 2025-02-25 (Gagan Bansal). It explains the redesigned v0.4 architecture. — [YouTube](https://www.youtube.com/watch?v=LM6JcqLeF0U)
  - https://www.youtube.com/watch?v=RLwyXRVvlNk, "Exploring multi-agent AI and AutoGen with Chi Wang", Foundation Capital, 51:29, 2024-05-24 (long interview). — [YouTube](https://www.youtube.com/watch?v=RLwyXRVvlNk)
- OUTDATED warning: the 2023 videos (Videos 1 and 2) show the original AutoGen v0.2 API (`AssistantAgent` / `UserProxyAgent`, `pyautogen`). Microsoft rebuilt the framework in v0.4 (see the LM6JcqLeF0U video above). Microsoft Developer also posted "Deep Dive into Microsoft Agent Framework for AutoGen Users" (https://www.youtube.com/watch?v=JlzteydCK_Q, found in search, about 11 months old; I did not check it with oEmbed). The paper's concepts still hold, but the old code will not match current releases.

#### 23. MetaGPT (Hong et al., 2023, arXiv 2308.00352)
Primary source: https://arxiv.org/abs/2308.00352 (code: https://github.com/FoundationAgents/MetaGPT)

- Video 1: https://www.youtube.com/watch?v=YtxMderNrzU
  - Title: "MetaGPT: Redefining Multi-Agent Collaboration for Complex Tasks" | Channel: What's AI by Louis-François Bouchard | 7:38 | Uploaded 2023-08-27
  - Note: A short, clear explainer for beginners on the paper's main idea: agents in software-company roles follow SOPs (standard operating procedures) and hand each other documents, which cuts down on errors compounding. It cites Hong et al. — [YouTube](https://www.youtube.com/watch?v=YtxMderNrzU)
  - Match: EXACT
- Video 2: https://www.youtube.com/watch?v=tFwYD1UPIfM
  - Title: "MetaGPT" | Channel: hu-po | 120:59 (a recorded livestream) | Uploaded 2023-08-15
  - Note: A two-hour live read-through of the arXiv paper (v3), for learners who want every detail. — [YouTube](https://www.youtube.com/watch?v=tFwYD1UPIfM)
  - Match: EXACT (long paper read)
- No talk by the MetaGPT authors (for example an ICLR 2024 oral) turned up on YouTube. Both videos cover an earlier arXiv version (v3) than the final ICLR paper.

#### 24. SWE-bench (Jimenez et al., 2023, arXiv 2310.06770)
Primary source: https://arxiv.org/abs/2310.06770 (leaderboard: https://www.swebench.com/)

- Video 1: https://www.youtube.com/watch?v=DrLdvbkgmeA
  - Title: "John Yang - SWE-bench: Can Language Models Resolve Real-World GitHub Issues?" | Channel: Rohan Alexander | 51:53 | Uploaded 2023-11-03
  - Note: A seminar talk by co-author John Yang (Princeton) on how the benchmark turns real GitHub issues and tests into tasks. — [YouTube](https://www.youtube.com/watch?v=DrLdvbkgmeA)
  - Match: EXACT (author talk)
- Video 2: https://www.youtube.com/watch?v=LgONGe838D0
  - Title: "SWE bench & SWE agent | Data Brew | Episode 44" | Channel: Databricks | 36:23 | Uploaded 2025-04-17
  - Note: Carlos Jimenez and Kilian Lieret (Princeton) explain SWE-bench and SWE-agent together, including data leakage and how agents get stuck in loops. It works for both item 24 and item 25. — [YouTube](https://www.youtube.com/watch?v=LgONGe838D0)
  - Match: EXACT (authors)
- Optional short clip: https://www.youtube.com/watch?v=bivZWNQHRfE, "SWE-Bench authors reflect on the state of LLM agents at Neurips 2024", Jay Alammar, 4:22, 2025-01-13 (Ofir Press and Carlos Jimenez). — [YouTube](https://www.youtube.com/watch?v=bivZWNQHRfE)
- Outdated note: the 2023 talk predates SWE-bench Verified and later versions, so leaderboard numbers in it are old.

#### 25. SWE-agent (Yang et al., 2024, arXiv 2405.15793)
Primary source: https://arxiv.org/abs/2405.15793

- Video 1: https://www.youtube.com/watch?v=RJ6NN8Y-xok
  - Title: "SWE-agent: A deep dive" | Channel: Ofir Press | 20:31 | Uploaded 2024-04-02
  - Note: Co-author Ofir Press explains how SWE-agent works and why they designed its agent-computer interface (ACI) the way they did. — [YouTube](https://www.youtube.com/watch?v=RJ6NN8Y-xok)
  - Match: EXACT (author)
- Video 2: https://www.youtube.com/watch?v=fcr8WzeEXyk
  - Title: "SWE-Agent Team Interview - Agents, Programming, and Benchmarks!" | Channel: Matthew Berman | 52:21 | Uploaded 2024-12-07
  - Note: A long interview with the SWE-agent team about the agent, programming and benchmarks. It is easy to follow for intermediate learners. — [YouTube](https://www.youtube.com/watch?v=fcr8WzeEXyk)
  - Match: EXACT
- Optional 2-minute demo: https://www.youtube.com/watch?v=CeMtJ4XObAM, "A First Look at SWE-agent", Carlos E. Jimenez, 2:19, 2024-04-01. — [YouTube](https://www.youtube.com/watch?v=CeMtJ4XObAM)
- Outdated note: Ofir Press's deep dive (April 2024) came out before the arXiv paper (May 2024) and uses GPT-4. The Matthew Berman interview links the newer swe-agent/swe-rex repos, so the tooling has moved on since the original paper.

### Inferences
- If only one video per item fits in the PDF, use these: 20 → LuarehusOWU, 21 → 0HljLKVdtjo, 22 → MCYzYzaWChY, 23 → YtxMderNrzU, 24 → DrLdvbkgmeA, 25 → RJ6NN8Y-xok.
- LgONGe838D0 (Data Brew) covers both items 24 and 25, so it could go under either one.
- Suggested beginner order for AutoGen: first the 2023 authors' talk for concepts, then the 8-minute v0.4 Research Forum video, so the learner knows the current API is different.

### Gaps
- I found no talk or video from Anthropic about how they built the Research system itself. The best options are a third-party walkthrough of the post and a related talk by an Anthropic architect.
- I found no handoffs-specific video from OpenAI itself, and the official Build Hour's description does not mention handoffs.
- I found no talk on YouTube by the MetaGPT authors (Sirui Hong et al.) or of an ICLR 2024 presentation.
- I took upload dates and durations from YouTube watch-page metadata, not from oEmbed, which does not return them.
