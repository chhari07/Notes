# Agentic AI reading list, Stages 1-2 (basics and tools): best YouTube videos per item

Verification method: every video below was checked on 2026-10-24 with `https://www.youtube.com/oembed?url=<url>&format=json`. All returned HTTP 200. Title and channel are copied exactly from oEmbed. Duration and upload date come from the watch page's `lengthSeconds` and `publishDate` fields. Primary source URLs were checked with curl (HTTP 200, or the redirect target noted).

## Which videos explain each item, with primary source and verified links

### Takeaway
Items 1, 2, 4, 6 and 8 have videos that cover that exact item. For items 1, 4 and 6 these include talks by the authors or the publisher (Anthropic / AI Engineer, Shunyu Yao, Timo Schick at Harvard CMSA). Items 3 (Wang et al. survey), 5 (MRKL) and 7 (Claude tool-use docs) have no strong video on the exact item, so the best related videos are given and labelled "closest match". The one exception is a short official Anthropic clip from 2024 for item 7, which is now dated.

### Cited Findings

#### 1. Building effective agents (Anthropic, Dec 2024)
Primary source: https://www.anthropic.com/research/building-effective-agents (HTTP 200)
- **Video A, EXACT (author talk).** https://www.youtube.com/watch?v=D7_ipDqhtwk. Title: "How We Build Effective Agents: Barry Zhang, Anthropic". Channel: AI Engineer. Duration 15:09. Uploaded 2025-04-04. Note: co-author Barry Zhang gives the core ideas of the post in a short talk: keep agents simple, build them only when the task needs one, and think from the agent's point of view. — [oEmbed/watch page](https://www.youtube.com/watch?v=D7_ipDqhtwk); the ai.engineer site lists it as a popular talk ([ai.engineer](https://ai.engineer/talks/D7_ipDqhtwk-effective-ai-agents))
- **Video B, EXACT (publisher).** https://www.youtube.com/watch?v=LP5OCa20Zpg. Title: "Tips for building AI agents". Channel: Anthropic. Duration 18:20. Uploaded 2025-02-13. Note: the post's authors (Barry Zhang, Erik Schluntz) talk with Alex Albert about workflows vs agents and common mistakes. The description links to the blog post. — [watch page](https://www.youtube.com/watch?v=LP5OCa20Zpg)
- Optional follow-up, EXACT-related (publisher). https://www.youtube.com/watch?v=uhJJgc-0iTQ. Title: "Building more effective AI agents". Channel: Anthropic. Duration 18:58. Uploaded 2025-10-17. Note: Erik, a co-author, explains how the advice changed over the next months (Agent SDK, Skills, MCP, multi-agent). — [watch page](https://www.youtube.com/watch?v=uhJJgc-0iTQ)

#### 2. LLM Powered Autonomous Agents (Lilian Weng, June 2023)
Primary source: https://lilianweng.github.io/posts/2023-06-23-agent/ (HTTP 200)
- **Video A, EXACT.** https://www.youtube.com/watch?v=_WIYPT5piaI. Title: "10 minutes paper (episode 27): LLM powered autonomous agents". Channel: CanConTech. Duration 39:22 (much longer than the title says). Uploaded 2023-08-02. Note: goes through Weng's post section by section: planning, memory and tool use. It is a small channel; the content is from 2023 but still matches the post. — [watch page](https://www.youtube.com/watch?v=_WIYPT5piaI)
- **Video B, EXACT (short skim).** https://www.youtube.com/watch?v=gQyaqrlv4F0. Title: "LLM Powered Autonomous Agents: Lilian Weng's Classic Essay, Read and Highlighted". Channel: Standarity. Duration 2:31. Uploaded 2026-08-22. Note: a very short highlighted read-through, good as a quick refresher. Small channel and low depth. — [watch page](https://www.youtube.com/watch?v=gQyaqrlv4F0)
- Closest-match alternative (well-known channel). https://www.youtube.com/watch?v=F8NKVhkZZWI. Title: "What are AI Agents?". Channel: IBM Technology. Duration 12:28. Uploaded 2024-07-15. Note: a beginner explainer of the same "LLM + planning + memory + tools" idea. It does not cover Weng's post itself. — [watch page](https://www.youtube.com/watch?v=F8NKVhkZZWI)

#### 3. A Survey on LLM-based Autonomous Agents (Wang et al., 2023)
Primary source: https://arxiv.org/abs/2308.11432 (HTTP 200). Later published in Frontiers of Computer Science 18(6), 2024 (from citing papers' reference lists).
- **No good video found for this exact survey.** YouTube-restricted searches for the title and for its framework (profile, memory, planning, action) found no walkthrough. — searches on youtube.com, 2026-10-24
- **Video A, CLOSEST MATCH.** https://www.youtube.com/watch?v=F8NKVhkZZWI. Title: "What are AI Agents?". Channel: IBM Technology. Duration 12:28. Uploaded 2024-07-15. Note: explains the parts of an agent (reasoning, memory, tools/action) that the survey organises into modules. — [watch page](https://www.youtube.com/watch?v=F8NKVhkZZWI)
- **Video B, CLOSEST MATCH.** https://www.youtube.com/watch?v=sal78ACtGTc. Title: "What's next for AI agentic workflows ft. Andrew Ng of AI Fund". Channel: Sequoia Capital. Duration 13:40. Uploaded 2024-03-26. Note: Andrew Ng's widely cited overview of agent design patterns (reflection, tool use, planning, multi-agent), a good map of the field the survey covers. — [watch page](https://www.youtube.com/watch?v=sal78ACtGTc)

#### 4. ReAct: Synergizing Reasoning and Acting in Language Models (Yao et al., 2022)
Primary source: https://arxiv.org/abs/2210.03629 (HTTP 200). ICLR 2023. Project page: https://react-lm.github.io
- **Video A, EXACT (paper explainer).** https://www.youtube.com/watch?v=QX-p-vsDoiQ. Title: "Keys to Understanding ReAct: Synergizing Reasoning and Acting in Language Models". Channel: Arize AI. Duration 43:14. Uploaded 2024-04-26. Note: a paper-reading session that walks through the ReAct paper, its Thought/Action/Observation loop and its results. — [watch page](https://www.youtube.com/watch?v=QX-p-vsDoiQ)
- **Video B, EXACT (first author).** https://www.youtube.com/watch?v=8t65bss7U74. Title: "Language Agents: From Reasoning to Acting — with Shunyu Yao of OpenAI, Harrison Chase of LangGraph". Channel: Latent Space. Duration 1:26:33. Uploaded 2024-09-27. Note: ReAct's first author explains where ReAct came from and how LangChain adopted it. It is a long podcast; use the chapter markers. — [watch page](https://www.youtube.com/watch?v=8t65bss7U74); chapters listed in search snippet ([search](https://www.youtube.com/watch?v=8t65bss7U74))
- Short beginner alternative. https://www.youtube.com/watch?v=vFdIrZyKEwQ. Title: "ReAct AI Agents, clearly explained!". Channel: Akshay Pachaar. Duration 5:45. Uploaded 2024-11-30. Note: a quick visual intro to the ReAct loop. — [watch page](https://www.youtube.com/watch?v=vFdIrZyKEwQ)
- Deeper author option. https://www.youtube.com/watch?v=zwfE6J2BIR4. Title: "Language Agents (Shunyu Yao PhD Defense)". Channel: Shunyu Yao. Duration 1:25:26. Uploaded 2024-05-10. Note: the author's thesis talk covering WebShop, ReAct, Tree of Thoughts and CoALA. Intermediate+. — [watch page](https://www.youtube.com/watch?v=zwfE6J2BIR4)

#### 5. MRKL Systems (Karpas et al., AI21 Labs, 2022)
Primary source: https://arxiv.org/abs/2205.00445 (HTTP 200)
- **No dedicated explainer video found for the MRKL paper.** YouTube-restricted searches for the title, "MRKL" and "Jurassic-X" turned up only LangChain "MRKL agent" tutorials and unrelated videos. — searches on youtube.com, 2026-10-24
- **Video A, CLOSEST MATCH (discusses MRKL directly).** https://www.youtube.com/watch?v=JaHfCrVTYF4. Title: "AI Agents as Neuro-Symbolic Systems?". Channel: James Briggs. Duration 28:59. Uploaded 2024-11-19. Note: the description says it is "thinking through AI agents and the neuro-symbolic definition from an early LLM agent paper called MRKL". It covers the router + expert-modules idea and its link to ReAct. — [watch page description](https://www.youtube.com/watch?v=JaHfCrVTYF4)
- Closest-match alternative. Reuse IBM Technology "What are AI Agents?" (https://www.youtube.com/watch?v=F8NKVhkZZWI). Note: IBM also has a written MRKL architecture page, https://www.ibm.com/architectures/hybrid/genai-mrkl (not a video). — [IBM](https://www.ibm.com/architectures/hybrid/genai-mrkl)

#### 6. Toolformer (Schick et al., Meta AI, 2023)
Primary source: https://arxiv.org/abs/2302.04761 (HTTP 200). NeurIPS 2023 oral.
- **Video A, EXACT (first author).** https://www.youtube.com/watch?v=UID_oXuN-0Y. Title: "Timo Schick | Toolformer: Language Models Can Teach Themselves to Use Tools". Channel: Harvard CMSA. Duration 55:42. Uploaded 2023-04-26. Note: the lead author explains how the model teaches itself API calls (calculator, search, QA, translation, calendar) and filters them by usefulness. — [watch page](https://www.youtube.com/watch?v=UID_oXuN-0Y)
- **Video B, EXACT (explainer).** https://www.youtube.com/watch?v=qvaxKDjAz4M. Title: "Deep Dive Into The Toolformer". Channel: Oxen. Duration 37:30. Uploaded 2024-02-12. Note: a paper-club walkthrough of the method and results in simpler terms. — [watch page](https://www.youtube.com/watch?v=qvaxKDjAz4M)
- Short alternative. https://www.youtube.com/watch?v=9gLIU65Er30. Title: "19. Toolformer: Language Models Can Teach Themselves to Use Tools (Schick et al., 2023)". Channel: LOADING_. Duration 7:50. Uploaded 2025-11-15. Note: a short summary, from a small channel. — [watch page](https://www.youtube.com/watch?v=9gLIU65Er30)
- Not found: no Yannic Kilcher or AI Coffee Break video on Toolformer turned up in searches.

#### 7. Tool use with Claude (Anthropic docs)
Primary source: https://platform.claude.com/docs/en/agents-and-tools/tool-use/overview (HTTP 200; the old docs.claude.com URL 302-redirects here)
- **Video A, EXACT but OUTDATED (publisher).** https://www.youtube.com/watch?v=6wkFb2_cUik. Title: "Tool use with the Claude 3 model family". Channel: Anthropic. Duration 2:13. Uploaded 2024-04-04. Note: Anthropic's official short launch video for tool use. The concepts still hold, but the model names and the "beta" status are out of date. — [watch page](https://www.youtube.com/watch?v=6wkFb2_cUik)
- **Video B, CLOSEST MATCH (hands-on tutorial).** https://www.youtube.com/watch?v=7xVmf9lIj14. Title: "Getting Started with Tool Use in the Anthropic API". Channel: Ram Vegiraju. Duration 14:04. Uploaded 2025-09-08. Note: a code walkthrough of defining tools and handling tool_use / tool_result in the Messages API. Links to code and docs. — [watch page description](https://www.youtube.com/watch?v=7xVmf9lIj14)
- Beginner concept alternative. https://www.youtube.com/watch?v=s-j_zDK0zKs. Title: "Claude Tool Calling Explained: How AI Agents Use Tools to Take Action Beyond Chat". Channel: DevOps Hint. Duration 10:02. Uploaded 2026-09-02 (recent). Note: explains the tool-calling flow with no code. Small channel. — [watch page](https://www.youtube.com/watch?v=s-j_zDK0zKs)

#### 8. Writing effective tools for agents (Anthropic, Sept 2025)
Primary source: https://www.anthropic.com/engineering/writing-tools-for-agents (308-redirects to https://www.anthropic.com/research/writing-tools-for-agents, which returns HTTP 200). One news item dates the post to 11 Sept 2025 ([blockchain.news](https://blockchain.news/ainews/anthropic-shares-best-practices-for-building-effective-tools-for-llm-agents-ai-developer-guide-2025)).
- **Video A, EXACT.** https://www.youtube.com/watch?v=07Ugw2WTjFk. Title: "Writing effective tools for AI agents (feat. Anthropic)". Channel: AI Papers. Duration 8:09. Uploaded 2026-07-27. Note: a chalkboard-style breakdown of the article: tools as contracts, evaluating tools, letting Claude Code improve them. — [watch page description](https://www.youtube.com/watch?v=07Ugw2WTjFk)
- **Video B, EXACT (short skim).** https://www.youtube.com/watch?v=ho_WzAGC80Q. Title: "Writing Effective Tools for AI Agents: Anthropic's Engineering Guide, Read and Highlighted". Channel: Standarity. Duration 2:48. Uploaded 2026-07-15. Note: a quick highlighted read-through. — [watch page](https://www.youtube.com/watch?v=ho_WzAGC80Q)
- Closest official alternative. Anthropic "Building more effective AI agents" (https://www.youtube.com/watch?v=uhJJgc-0iTQ, 18:58, 2025-10-17). Note: covers best practices for tools, MCP servers and skills, from Anthropic itself. — [watch page description](https://www.youtube.com/watch?v=uhJJgc-0iTQ)

### Inferences
- The best primary-source videos are item 1 (Barry Zhang, AI Engineer), item 4 (Shunyu Yao / Latent Space) and item 6 (Timo Schick / Harvard CMSA). They come straight from the authors and are the most trustworthy picks for the PDF.
- The two videos for item 8 are both from small channels. Pair them with the Anthropic video uhJJgc-0iTQ for an authoritative voice.
- For item 7, the official Anthropic video is from the Claude 3 era (April 2024). Learners should treat the docs page as the main source and the video only as a concept intro.
- The "Standarity" videos (items 1, 2, 8) are about 2-3 minute skims. They are fine as refreshers, not as main explainers.

### Gaps
- I found no video that walks through the Wang et al. survey (item 3) or the MRKL paper itself (item 5). The videos given are closest matches.
- I did not watch the videos in full. Quality notes rely on the title, description, chapter list, channel and length.
- Search did not surface an Anthropic-made video built specifically around the "Writing effective tools for agents" post.
- Not verified: whether Yannic Kilcher, AI Coffee Break, Sam Witteveen or DeepLearning.AI have videos on these exact papers. None appeared in searches.
