# Stages 3-4: RAG and Output Control, YouTube Videos (Items 9-15)

Method: I found candidates by scraping YouTube search results (title, channel, duration, age and views come from the results page). Every video below was then checked on 2026-10-24 via `https://www.youtube.com/oembed?url=...&format=json`, and the title and channel are exactly what oEmbed returned. All of them passed. Upload years are exact where I read the watch page's uploadDate. Otherwise they are worked out from YouTube's "N years ago" label, which is approximate. Primary source URLs were checked with curl and returned HTTP 200 (or a redirect, noted where it happened).

## Which videos explain each exact item, and what is the primary source?

### Takeaway
Six of the seven items have an exact-match video. Three are by the authors or the publishing org: Patrick Lewis on RAG, Akari Asai on Self-RAG, and OpenAI DevDay on Structured Outputs. The Outlines item has a talk by co-author Remi Louf. Self-RAG and CRAG are both covered by LangChain's official LangGraph videos. For Anthropic's context-engineering post, the best exact match is a third-party walkthrough (Dave Ebbelaar). For Anthropic's Streaming Messages docs I found no trustworthy video, so only a closest match on the underlying technology (Server-Sent Events) is given.

### Cited Findings

#### 9. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks (Lewis et al., 2020)
- Primary source: https://arxiv.org/abs/2005.11401 (HTTP 200)
- Video A (EXACT, by the first author): https://www.youtube.com/watch?v=JGpmQvlYRdU
  - Title: "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks, with Patrick Lewis, Facebook AI"
  - Channel: Natural Language Processing presentations | Duration: 1:22:32 | Uploaded: 2020 (2020-07-07)
  - Note: Patrick Lewis presents his own paper at an NY-NLP meetup (2 July 2020). It is the clearest first-hand explanation of how the retriever and generator work together. It is long and fairly technical. — [Video page description](https://www.youtube.com/watch?v=JGpmQvlYRdU)
- Video B (closest match, general RAG concept): https://www.youtube.com/watch?v=T-D1OfcDW1M
  - Title: "What is Retrieval-Augmented Generation (RAG)?"
  - Channel: IBM Technology | Duration: 6:36 | Uploaded: ~2023 | ~2.07M views
  - Note: A short, beginner-friendly whiteboard intro to why RAG reduces out-of-date and made-up answers. Watch it before Video A. It covers the idea, not the paper.

#### 10. Self-RAG (Asai et al., 2023)
- Primary source: https://arxiv.org/abs/2310.11511 (HTTP 200). Project page (not checked): https://selfrag.github.io/
- Video A (EXACT, by the first author): https://www.youtube.com/watch?v=bVz8Ua1VVsE
  - Title: "Akari Asai: Self-reflective Language Models with Retrieval (2023-10-26)"
  - Channel: UMass Machine Learning & Friends Lunch | Duration: 1:00:09 | Uploaded: 2024 (2024-01-06; talk given 2023-10-26)
  - Note: Akari Asai explains why models hallucinate and how Self-RAG uses special "reflection tokens" to decide when to retrieve and how to critique its own output. — [Video page description](https://www.youtube.com/watch?v=bVz8Ua1VVsE)
- Video B (EXACT, practical implementation): https://www.youtube.com/watch?v=pbAd8O1Lvm4
  - Title: "Self-reflective RAG with LangGraph: Self-RAG and CRAG"
  - Channel: LangChain | Duration: 17:38 | Uploaded: ~2024 | ~39.7K views
  - Note: LangChain's official video turns the Self-RAG idea into a LangGraph flow (grade documents, check for hallucinations, retry). Good for builders. It is a simplified version: prompts stand in for the paper's trained reflection tokens. — the matching blog post is [LangChain blog](https://blog.langchain.com/agentic-rag-with-langgraph)
- Optional extra (author, newer and broader): https://www.youtube.com/watch?v=uoM32c4BQ-g, "CMU Advanced NLP Spring 2026 (10): Akari Asai - Retrieval, RAG, and Deep Research", channel Sean Welleck, 1:17:34, ~2026. It is an up-to-date lecture on RAG by the Self-RAG author (oEmbed verified).

#### 11. Corrective RAG / CRAG (Yan et al., 2024)
- Primary source: https://arxiv.org/abs/2401.15884 (HTTP 200)
- Video A (EXACT): https://www.youtube.com/watch?v=pbAd8O1Lvm4
  - Title: "Self-reflective RAG with LangGraph: Self-RAG and CRAG"
  - Channel: LangChain | Duration: 17:38 | Uploaded: ~2024
  - Note: The same LangChain video as item 10. It also covers CRAG's main idea: grade the retrieved documents, and fall back to web search when they are not relevant. LangChain's version skips the paper's optional "knowledge refinement" step. — [LangChain blog](https://blog.langchain.com/agentic-rag-with-langgraph)
- Video B (EXACT, hands-on): https://www.youtube.com/watch?v=E2shqsYwxck
  - Title: "Building Corrective RAG from scratch with open-source, local LLMs"
  - Channel: LangChain | Duration: 26:00 | Uploaded: ~2024 | ~106K views
  - Note: A step-by-step build of CRAG with LangGraph and a local model. You can follow along without paid APIs. Some LangChain APIs shown may have changed since 2024.

#### 12. Effective context engineering for AI agents (Anthropic, 2025)
- Primary source: https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents. Note: this now redirects (HTTP 308) to https://www.anthropic.com/research/effective-context-engineering-for-ai-agents (HTTP 200). Either link works, but the /research/ URL is the final one.
- Video A (EXACT, third-party walkthrough of the post): https://www.youtube.com/watch?v=nkJXADeI62c
  - Title: "Effective Context Engineering for AI Agents (why agents still fail in practice)"
  - Channel: Dave Ebbelaar | Duration: 25:03 | Uploaded: 2025 (2025-12-19) | ~29K views
  - Note: Walks through Anthropic's post itself: what context engineering is, tips for system prompts, and common pitfalls. Its description links straight to the Anthropic article. — [Video page description](https://www.youtube.com/watch?v=nkJXADeI62c)
- Video B (closest match, same concept from another well-known org): https://www.youtube.com/watch?v=4GiqzUHD5AA
  - Title: "Context Engineering for Agents"
  - Channel: LangChain | Duration: 22:06 | Uploaded: ~2025 | ~204K views
  - Note: Lance Martin groups context-engineering strategies (write, select, compress, isolate). It pairs well with Anthropic's post but is not about that post.
- Optional extra (official Anthropic channel, short): https://www.youtube.com/watch?v=eW3oTyfeWZ0, "Context Management in Claude Code", channel Claude, 3:31, ~2026 (oEmbed verified). It shows context management inside Claude Code, a narrower product view.

#### 13. Introducing Structured Outputs in the API (OpenAI, Aug 2024)
- Primary source: https://openai.com/index/introducing-structured-outputs-in-the-api/. curl got HTTP 403, which is OpenAI's bot protection and normal for openai.com. This is the official URL of the August 2024 announcement.
- Video A (EXACT, by the publishing org): https://www.youtube.com/watch?v=kE4BkATIl9c
  - Title: "OpenAI DevDay 2024 | Structured outputs for reliable applications"
  - Channel: OpenAI | Duration: 40:40 | Uploaded: 2024 (2024-12-17) | ~98K views
  - Note: The OpenAI engineers who built the feature (Atty Eleti and Michelle Pokrass) explain how it guarantees JSON Schema adherence and how it works under the hood. — speakers confirmed by [Simon Willison's DevDay live blog](https://simonwillison.net/2024/Oct/1/openai-devday-2024-live-blog)
- Video B (EXACT, practical tutorial): https://www.youtube.com/watch?v=fuMKrKlaku4
  - Title: "OpenAI Structured Output - All You Need to Know"
  - Channel: Dave Ebbelaar | Duration: 24:46 | Uploaded: ~2024 | ~65K views
  - Note: A hands-on Python and Pydantic walkthrough of the feature. Model names and SDK calls may be slightly out of date by 2026.

#### 14. Efficient Guided Generation for Large Language Models (Willard & Louf, 2023; Outlines)
- Primary source: https://arxiv.org/abs/2307.09702 (HTTP 200). Library (not checked): https://github.com/dottxt-ai/outlines
- Video A (EXACT, by co-author Remi Louf): https://www.youtube.com/watch?v=aNmfvN6S_n4
  - Title: "No more bad outputs with structured generation: Remi Louf"
  - Channel: AI Engineer | Duration: 15:32 | Uploaded: 2024 (AI Engineer World's Fair 2024) | ~10.9K views
  - Note: The Outlines co-author shows how limiting which tokens the model may pick (regex, JSON Schema, Pydantic) gives reliable outputs. — [AI Engineer talk page](https://ai.engineer/worldsfair/2024/schedule/no-more-bad-outputs-with-structured-generation)
- Video B (EXACT on the paper's method, explainer): https://www.youtube.com/watch?v=xpvFinvqRCA
  - Title: "Structured Output from LLMs: Grammars, Regex, and State Machines"
  - Channel: Efficient NLP | Duration: 17:20 | Uploaded: ~2025 | ~12.8K views
  - Note: Explains the core trick of the paper visually: turning a regex or grammar into a finite-state machine that masks out invalid tokens.
- Optional extra (publishing org): https://www.youtube.com/watch?v=vEF-nuf_zRM, "Working with LLMs: JSON Mode vs Structured Generation", channel dottxt (the company behind Outlines), 10:03, ~2024 (oEmbed verified).

#### 15. Streaming messages (Anthropic docs)
- Primary source: https://platform.claude.com/docs/en/build-with-claude/streaming (HTTP 200). The old URL https://docs.claude.com/en/docs/build-with-claude/streaming redirects (302) to it.
- Video A (CLOSEST MATCH, underlying technology): https://www.youtube.com/watch?v=4HlNv1qpZFY
  - Title: "Server-Sent Events Crash Course"
  - Channel: Hussein Nasser | Duration: 29:48 | Uploaded: ~2020 | ~128K views
  - Note: Explains Server-Sent Events (SSE), the protocol Claude's streaming API uses to send text bit by bit. It is not Claude-specific, so read the Anthropic docs for event names like message_start and content_block_delta.
- Exact-match video: no good video found. The candidates were all small channels. The most-viewed one, "10. Response streaming - Building with the Claude API - Claude course" (channel "Claude Courses", ItT1fsIvt9E), looks like an unofficial re-upload: its description pushes a link-shortener "guided notes" URL. I left it out.

### Inferences
- Suggested beginner order where two videos exist: watch the short or concept video first (IBM for RAG, LangChain for Self-RAG and CRAG, Remi Louf for Outlines), then the longer author talk.
- The LangChain video pbAd8O1Lvm4 can be cited for both items 10 and 11. In the PDF, either list it under both items or cross-reference it.
- Item 15 can lean on the docs alone. The Anthropic docs page has code samples, which beginners may find clearer than a third-party video.

### Gaps
- Exact upload dates were read only for JGpmQvlYRdU, bVz8Ua1VVsE, nkJXADeI62c and kE4BkATIl9c. The others are approximate, from YouTube's relative "N years ago" labels on the search page as of 2026-10-24.
- I found no official Anthropic video on the "Effective context engineering" post, and no official Anthropic video on streaming. One may exist on the Claude channel or in Anthropic Academy courses that YouTube search did not show.
- I found no Yannic Kilcher or AI Coffee Break video on the 2020 RAG paper itself. Yannic covers REALM, a related but different paper.
- I did not watch the videos in full. The "why it's useful" notes come from titles, descriptions, chapter lists and the channels' known focus.
