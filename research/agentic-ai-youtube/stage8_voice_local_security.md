# Stage 8: Voice, running models locally, and security (items 26-30): YouTube videos

Method: I found the videos by scraping YouTube search results (ytInitialData). I checked every URL below with `https://www.youtube.com/oembed?url=<URL>&format=json` on 2026-10-24, and all of them returned 200. Titles and channels are copied exactly from oEmbed. Durations and upload dates come from each watch page (`lengthSeconds` and `uploadDate`). No video ID was guessed.

## 26. Whisper: Robust Speech Recognition via Large-Scale Weak Supervision (Radford et al., 2022)

### Takeaway
Primary source: https://arxiv.org/abs/2212.04356. There are several paper walkthroughs. The best two are by Aleksa Gordić (paper plus code, 1 hour) and Aladdin Persson (33 min). For a quick beginner overview, use the 5-minute video by What's AI. OpenAI has no official video explaining the paper.

### Cited Findings
- **Video 1 (exact match):** https://www.youtube.com/watch?v=AwJf8aQfChE
  - Title: "OpenAI Whisper: Robust Speech Recognition via Large-Scale Weak Supervision | Paper and Code"
  - Channel: Aleksa Gordić - The AI Epiphany
  - Length 1:02:41, uploaded 2022-09-24
  - Note: Walks through the paper and then the open-source code, so you see how the encoder-decoder model and its special task tokens work in practice.
  - Source: [oEmbed/watch page](https://www.youtube.com/watch?v=AwJf8aQfChE)
- **Video 2 (exact match):** https://www.youtube.com/watch?v=Kh058oMt-08
  - Title: "Whisper Paper Explained: Robust Speech Recognition via Large-Scale Weak Supervision"
  - Channel: Aladdin Persson
  - Length 0:33:16, uploaded 2022-12-15
  - Note: A shorter, step-by-step reading of the paper covering the data, the model and the results.
  - Source: [watch page](https://www.youtube.com/watch?v=Kh058oMt-08)
- **Optional beginner intro (exact match, short):** https://www.youtube.com/watch?v=uFOkMme19Zs
  - Title: "OpenAI's Whisper Model Explained"
  - Channel: What's AI by Louis-François Bouchard
  - Length 0:05:24, uploaded 2022-10-05
  - Note: A 5-minute, plain-English summary of what Whisper is and why 680k hours of weakly labelled audio matter.
  - Source: [watch page](https://www.youtube.com/watch?v=uFOkMme19Zs)
- The paper describes models trained on 680,000 hours of internet audio-transcript pairs, which work zero-shot. — [arXiv 2212.04356](https://arxiv.org/abs/2212.04356)

### Inferences
- All three videos date from 2022, but the paper has not changed, so they are not out of date for this item. They do not cover later variants such as large-v3 or turbo.

### Gaps
- I found no talk by the paper's authors (OpenAI) explaining Whisper.

## 27. Voice agents guide (OpenAI docs: chained STT -> LLM -> TTS vs. realtime speech-to-speech)

### Takeaway
Primary source: the OpenAI Voice agents guide, https://developers.openai.com/api/docs/guides/voice-agents (also reachable at https://developers.openai.com/docs/guides/voice-agents). Both talks below are by OpenAI staff and directly compare the chained and speech-to-speech designs, so they are exact matches.

### Cited Findings
- **Video 1 (exact match):** https://www.youtube.com/watch?v=iXhba366fQc
  - Title: "Building voice agents with OpenAI — Dominik Kundel, OpenAI"
  - Channel: AI Engineer
  - Length 1:25:35, uploaded 2025-06-29
  - Note: A hands-on workshop. The description says it covers "the differences between chained and speech-to-speech powered voice agents" and turns a text agent into a voice agent.
  - Source: [watch page](https://www.youtube.com/watch?v=iXhba366fQc)
- **Video 2 (exact match, short):** https://www.youtube.com/watch?v=-OXiljTJxQU
  - Title: "Building Effective Voice Agents — Toki Sherbakov + Anoop Kotha, OpenAI"
  - Channel: AI Engineer
  - Length 0:17:17, uploaded 2025-07-20
  - Note: A 17-minute talk by OpenAI solution architects on chained vs. speech-to-speech trade-offs (latency, control) and lessons from customers.
  - Sources: [watch page](https://www.youtube.com/watch?v=-OXiljTJxQU); the talk page lists a chapter on chained vs. speech-to-speech at about 4:29 ([ai.engineer](https://ai.engineer/talks/building-effective-voice-agents))
- **Optional, official OpenAI channel:** https://www.youtube.com/watch?v=rpj1m0wYs8M
  - Title: "Build Hour: Voice Agents"
  - Channel: OpenAI
  - Length 0:54:41, uploaded 2025-09-02
  - Note: Demos speech-to-speech agents built with the Realtime API and the Agents SDK.
  - Source: [watch page](https://www.youtube.com/watch?v=rpj1m0wYs8M)
- **Optional, launch video:** https://www.youtube.com/watch?v=nfBbmtMJhX0
  - Title: "Introducing gpt-realtime in the API"
  - Channel: OpenAI
  - Length 0:17:54, uploaded 2025-08-28
  - Note: The launch of the general-availability speech-to-speech model.
  - Source: [watch page](https://www.youtube.com/watch?v=nfBbmtMJhX0)
- The OpenAI docs recommend speech-to-speech for low-latency conversation and the chained design for predictable workflows, or when you are extending a text agent. — [OpenAI voice agents guide](https://developers.openai.com/docs/guides/voice-agents)

### Inferences
- These videos are about 15 months old. Model names have moved on: search results show newer launches, for example a video titled "GPT-Live-1" from about a month ago. The chained vs. speech-to-speech concepts still hold.

### Gaps
- I did not confirm which of the two developers.openai.com URL paths is canonical. Both appeared in search results.

## 28. Ollama and llama.cpp (running open models locally)

### Takeaway
Primary sources: https://github.com/ollama/ollama and https://github.com/ggml-org/llama.cpp. IBM Technology has short, beginner-friendly explainers for each tool, so one video per tool is an exact match. Tech With Tim is good for a hands-on Ollama setup, and Alex Ziskind compares the two tools.

### Cited Findings
- **Video 1, Ollama (exact match):** https://www.youtube.com/watch?v=5RIOQuHOihY
  - Title: "What is Ollama? Running Local LLMs Made Simple"
  - Channel: IBM Technology
  - Length 0:07:13, uploaded 2025-04-08
  - Note: A 7-minute concept intro to running models locally with one command.
  - Source: [watch page](https://www.youtube.com/watch?v=5RIOQuHOihY)
- **Video 2, llama.cpp (exact match):** https://www.youtube.com/watch?v=P8m5eHAyrFM
  - Title: "What Is Llama.cpp? The LLM Inference Engine for Local AI"
  - Channel: IBM Technology
  - Length 0:09:14, uploaded 2026-03-16
  - Note: Cedric Clyburn explains what the engine under Ollama does (GGUF, quantization, running on a CPU or laptop).
  - Source: [watch page](https://www.youtube.com/watch?v=P8m5eHAyrFM)
- **Optional hands-on:** https://www.youtube.com/watch?v=UtSSMs6ObqY
  - Title: "Learn Ollama in 15 Minutes - Run LLM Models Locally for FREE"
  - Channel: Tech With Tim
  - Length 0:14:01, uploaded 2025-01-13
  - Note: An install-and-use walkthrough. At about 1.28M views it is the most-viewed Ollama tutorial in the search results.
  - Source: [watch page](https://www.youtube.com/watch?v=UtSSMs6ObqY)
- **Optional comparison:** https://www.youtube.com/watch?v=2t9XrPcAiHg
  - Title: "Local AI just leveled up... Llama.cpp vs Ollama"
  - Channel: Alex Ziskind
  - Length 0:14:40, uploaded 2025-11-14
  - Note: Shows the llama.cpp web UI and GGUF setup side by side with Ollama.
  - Source: [watch page](https://www.youtube.com/watch?v=2t9XrPcAiHg)
- Ollama is a wrapper around llama.cpp, and llama.cpp gives lower-level control over loading, quantization and memory. — [UDel workshop notes](https://lem.che.udel.edu/git/furst/llm-workshop/raw/branch/main/02-ollama/README.md)

### Inferences
- NetworkChuck's only result was a 40-second Short (piFDfCaISk8), so I left it out. I did not see a full NetworkChuck Ollama video in the results.

### Gaps
- I found no talk by Georgi Gerganov (llama.cpp/ggml) or by the Ollama team in the search results.

## 29. Not what you've signed up for: Indirect Prompt Injection (Greshake et al., 2023)

### Takeaway
Primary source: https://arxiv.org/abs/2302.12173. The paper's authors gave a talk at Black Hat USA 2023, "Compromising LLMs: The Advent of AI Malware", which is on the official Black Hat channel. That is the exact match. Simon Willison's 12-minute explainer is the best beginner companion (closest match: it covers prompt injection in general, including the indirect kind).

### Cited Findings
- **Video 1 (exact match, by the authors):** https://www.youtube.com/watch?v=5DoDxqQJIQ8
  - Title: "Compromising LLMs: The Advent of AI Malware"
  - Channel: Black Hat
  - Length 0:36:28, uploaded to YouTube 2024-01-29 (talk given at Black Hat USA 2023)
  - Note: The paper's authors (Sahar Abdelnabi, Christoph Endres, Mario Fritz, Kai Greshake, Shailesh Mishra, as listed in the description) show how hidden instructions in web pages and emails take over LLM apps.
  - Sources: [watch page](https://www.youtube.com/watch?v=5DoDxqQJIQ8); Simon Willison calls it "The big Black Hat 2023 Prompt Injection talk, by Kai Greshake and team" ([simonwillison.net](https://blog.simonwillison.net/2023/Aug/18/compromising-llms/))
- **Video 2 (closest match, beginner):** https://www.youtube.com/watch?v=FgxwCaL6UTA
  - Title: "Prompt Injection, explained"
  - Channel: Simon Willison
  - Length 0:12:16, uploaded 2023-05-03
  - Note: The person who coined the term explains, in plain words, why mixing trusted instructions with untrusted text is dangerous. The examples include email assistants, which is the indirect case.
  - Source: [watch page](https://www.youtube.com/watch?v=FgxwCaL6UTA)
- **Optional short explainer:** https://www.youtube.com/watch?v=s_Ztu6c-IGQ
  - Title: "Episode 4: Indirect Prompt Injection Explained | AI Red Teaming 101"
  - Channel: Microsoft Developer
  - Length 0:06:28, uploaded 2025-07-09
  - Note: A 6-minute explainer, from Microsoft's ADAPT red team, of instructions hidden in emails, websites and documents.
  - Source: [watch page](https://www.youtube.com/watch?v=s_Ztu6c-IGQ)
- An unofficial mirror of the Black Hat talk exists on the "sequire technology" channel (WIEy4eiQFPM). Prefer the official Black Hat upload. — [YouTube search results](https://www.youtube.com/results?search_query=Compromising+LLMs+the+advent+of+AI+malware+Black+Hat)

### Inferences
- The Black Hat talk covers the paper's attack taxonomy and demos, so it can stand in for reading the paper.

### Gaps
- I found no separate Kai Greshake solo talk on YouTube. The Robust Intelligence interview is hosted on their own site, and I did not confirm a YouTube copy. — [Robust Intelligence](https://www.robustintelligence.com/resource-center/ai-security-interview-series-pushing-the-boundaries-of-prompt-injection-attacks)

## 30. OWASP Top 10 for LLM Applications (2025) and OWASP Mobile Top 10

### Takeaway
There is an important version issue. An OWASP Top 10 for LLM Applications 2026 edition was reportedly released in early August 2026, so the 2025 list in the reading list is now one version behind. The official genai.owasp.org page I fetched still showed 2025 as current. Mobile Top 10: the latest edition is 2024 (final).

### Primary sources
- 2025 LLM list: https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/
- Hub: https://genai.owasp.org/llm-top-10/
- Mobile: https://owasp.org/www-project-mobile-top-10/

### Cited Findings
- **Video 1, LLM Top 10 (exact match, beginner):** https://www.youtube.com/watch?v=gUNXZMcd2jU
  - Title: "OWASP's Top 10 Ways to Attack LLMs: AI Vulnerabilities Exposed"
  - Channel: IBM Technology
  - Length 0:25:11, uploaded 2026-03-07
  - Note: Jeff Crume walks through the list (prompt injection, data leaks and others) with defenses. It was uploaded after the 2025 list came out and before the 2026 one, so it almost certainly covers 2025. The description does not state the edition.
  - Source: [watch page](https://www.youtube.com/watch?v=gUNXZMcd2jU)
- **Video 2, LLM Top 10 (from OWASP itself):** https://www.youtube.com/watch?v=1xUTxLhV07g
  - Title: "OWASP Top 10 for Large Language Models: Project Update - Steve Wilson, Scott Clinton"
  - Channel: OWASP Foundation
  - Length 0:45:35, uploaded 2025-03-21
  - Note: The project leads explain the project and the 2025 update. This is the official OWASP-channel source.
  - Source: [watch page](https://www.youtube.com/watch?v=1xUTxLhV07g)
- **Optional, newer 2026 edition:** https://www.youtube.com/watch?v=auS34nm9VAc
  - Title: "The OWASP LLM Top 10 has a few surprises for you"
  - Channel: IBM Technology
  - Length 0:29:05, uploaded 2026-08-12
  - Note: A podcast segment (0:00–12:55) on the 2026 list and its new incident-data weighting. Watch this to see what changed after 2025.
  - Source: [watch page](https://www.youtube.com/watch?v=auS34nm9VAc)
- **Video 3, Mobile Top 10 (exact match, 2024 edition):** https://www.youtube.com/watch?v=DG9IySbCBRc
  - Title: "What Is The OWASP Mobile Top 10?"
  - Channel: UnderSecured
  - Length 0:21:02, uploaded 2025-01-06
  - Note: A 21-minute beginner walkthrough of each mobile risk category from a pentester's view.
  - Source: [watch page](https://www.youtube.com/watch?v=DG9IySbCBRc)
- **Video 4, Mobile Top 10 (exact match, deep dive):** https://www.youtube.com/watch?v=MXbuEyzDp6A
  - Title: "OWASP Mobile Top 10 Risks  (2024) |  Detailed Explaination with Examples | Payatu"
  - Channel: Payatu
  - Length 2:07:24, uploaded 2024-05-03
  - Note: A long webinar on the 2024 changes, with scenarios and examples for each risk.
  - Source: [watch page](https://www.youtube.com/watch?v=MXbuEyzDp6A)
- **Outdated, do not use as the main video:** https://www.youtube.com/watch?v=cYuesqIKf9A
  - Title: "Explained: The OWASP Top 10 for Large Language Model Applications"
  - Channel: IBM Technology
  - Uploaded 2023-09-01
  - Note: Covers the original 2023 v1 list, which predates the 2025 list.
  - Source: [watch page](https://www.youtube.com/watch?v=cYuesqIKf9A)

#### 2025 list contents
- The 2025 list runs LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, LLM03 Supply Chain, LLM04 Data and Model Poisoning, LLM05 Improper Output Handling, LLM06 Excessive Agency, LLM07 System Prompt Leakage, LLM08 Vector and Embedding Weaknesses, LLM09 Misinformation, LLM10 Unbounded Consumption. The previous edition was v1.1, dated 2024-04-11. — [genai.owasp.org](https://genai.owasp.org/llm-top-10/)

#### 2026 edition (the sources disagree)
- **Release date:** A 2026 edition was reported as published on 2026-08-04. One CSA note dates it 2026-08-03. — [Cyber Security News](https://cybersecuritynews.com/owasp-genai-llm-top-10-2026/amp/); [CSA](https://labs.cloudsecurityalliance.org/research/csa-research-note-owasp-llm-top10-2026-incident-weighted-202/)
- **What it reportedly changed:** Rankings now weight community votes at about 75% and incident data for the rest. Excessive Agency rose to #3, Improper Output Handling fell to #10, and System Prompt Leakage was renamed Hidden Context Exposure. — [CSA](https://labs.cloudsecurityalliance.org/research/csa-research-note-owasp-llm-top10-2026-incident-weighted-202/); [Superblocks](https://www.superblocks.com/blog/owasp-llm-top-10)
- **Conflict:** The genai.owasp.org/llm-top-10 page I fetched still shows the 2025 list as current. That may be a cached or outdated page, or the 2026 edition may be hosted elsewhere. — [genai.owasp.org](https://genai.owasp.org/llm-top-10/)
- **Agentic list:** OWASP also publishes a separate Top 10 for Agentic Applications, reported as released in December 2025. — [Cyber Security News](https://cybersecuritynews.com/owasp-genai-llm-top-10-2026/amp/)

#### Mobile Top 10
- The OWASP Mobile Top 10 project page says: "The new Mobile Top 10 list for 2024 is out now". — [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/)

### Inferences
- For a 2026 study list, use the 2025 videos for the item as written, and add the IBM 2026 podcast as an "update" pointer. Consider also linking the OWASP Agentic Top 10, since it fits an agentic AI study list.

### Gaps
- I did not independently confirm the official 2026 LLM Top 10 document on genai.owasp.org. The fetched page showed 2025 only.
- I found no OWASP-channel video dedicated to the Mobile Top 10 2024. The OWASP Egypt chapter video (1ipJMu6xkKM) is from 4 years ago, which predates the 2024 list.
- I did not confirm from the video itself which list edition gUNXZMcd2jU covers.
