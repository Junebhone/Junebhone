# Bhone Kyaw Si Hein

**AI & automation engineer with production full-stack experience.**
I build LLM agents and orchestration layers that automate real work — and ship the products around them, end to end.

📍 Houston, TX &nbsp;·&nbsp; 🌐 [bhonekyawsihein.tech](https://bhonekyawsihein.tech) &nbsp;·&nbsp; 🎓 M.S. Engineering Data Science & AI, University of Houston (Dec 2026) &nbsp;·&nbsp; 💼 **Open to AI / ML engineering and automation roles**

---

## What I do

**Build LLM agents that do real work.** LangChain / LangGraph orchestration, tool routing, RAG pipelines, multimodal calls. The interesting part isn't the prompt — it's designing tool boundaries and fallback paths so the agent *fails explicitly* instead of hallucinating when a tool returns nothing usable.

**Give agents real tools, not toy ones.** Wrapping live external APIs as agent tools means handling the unglamorous parts: rate limits, auth, partial failures, and the difference between a call that broke and a call that legitimately returned nothing. In the Spatial Omics Copilot that meant Enrichr, NCBI Gene, and PubMed behind a structured tool interface with an explicit call budget.

**Ship the whole product.** Next.js and React Native front ends, Node.js + PostgreSQL back ends, Stripe payments, production deploys, and the support retainer afterwards. Two published iOS apps.

---

## Selected work

### Open source

| Project | What it is |
|---|---|
| **[officeqa-financial-rag](https://github.com/Junebhone/officeqa-financial-rag)** | Financial RAG over U.S. Treasury Bulletins (Databricks OfficeQA benchmark). Baseline vs. engineered pipeline, measured across six metrics. Structure-aware chunking plus year/month metadata pre-filtering took **Doc Hit Rate@5 from 11.8% → 58.8%** and Recall@5 from 5.9% → 47.1%. Includes the honest write-up of *why* factual accuracy stays near-zero — retrieval finds the right bulletin but never the exact cell, and most gold answers are derived statistics never printed in the source. <br>`Python` · `ChromaDB` · `bge-small` · `Ollama / qwen2.5` |
| **[weather-aware-assistant](https://github.com/Junebhone/weather-aware-assistant)** | CLI assistant that reads a calendar, checks live weather per event, and synthesises practical advice. Zero dependencies, zero API keys, **88 offline tests**. Architected so logic never prints and UI never decides — the advice engine is a pure function. <br>`Python` · `Open-Meteo` |
| **[Ingenico](https://github.com/Junebhone/Ingenico)** | React Native app running on an Ingenico Android POS terminal. A custom native module bridges JS to the terminal's `UVectorPrinter` AIDL service, and Pusher WebSockets push print jobs to the device in real time. <br>`React Native` · `Java` · `AIDL` · `Pusher` |
| **[Estify](https://github.com/Junebhone/Estify)** | Laravel classified-ads marketplace. Every listing sits inside two independent three-level hierarchies — category/subcategory/childcategory and country/state/city — with a role-gated admin panel over both and FilePond uploads that validate and orient photos client-side. <br>`Laravel` · `Jetstream` · `Tailwind` · `Alpine.js` |
| **[mini-corebanking](https://github.com/Junebhone/mini-corebanking)** | Core-banking prototype built during my internship at uab bank — customer onboarding, account lifecycle, deposit/withdraw/transfer workflows, and reporting over a normalised MySQL schema. <br>`PHP` · `MySQL` · `Tailwind` |

### Team projects

**[Spatial Omics Copilot](https://github.com/alexthefirst99/Spatial-Omics-Copilot)** — a RAG chatbot that lets researchers query spatial transcriptomics data in plain English. Built by a team of 6; I'm the second-largest contributor and **own the agent layer** (`src/rag/copilot_agent/`).

What I built there:

- **LangGraph orchestration and a deterministic router.** The router picks which evidence tools a question needs — pathway enrichment, NCBI Gene annotation, PubMed — from the question alone. I made it rule-based rather than LLM-driven on purpose: every tool does live network I/O, the agent is capped at five tool calls per turn, and a mis-parsed instruction shouldn't be allowed to spend that budget. It's also the only way routing decisions stay assertable in tests without a live model.
- **Tool boundaries that fail honestly.** Each tool returns a structured outcome that distinguishes *"the call failed"* from *"the call succeeded and found nothing"* — so the agent reports an empty result instead of narrating one.
- **Multimodal payload construction and the DeepInfra client**, plus semantic re-ranking of retrieved abstracts against the question.
- **The agent test suite**, and a round of fixes resolving 10 findings from an adversarial review.

One bug worth keeping: an early router matched terms as prefixes, so `"color"` matched **"colorectal"** — silently routing questions about the project's own demo tissue down the image branch and running no evidence tools at all. Inflections are now listed explicitly. More typing, far fewer surprises.

`Python` · `LangGraph` · `LangChain` · `DeepInfra` · Enrichr / NCBI Gene / PubMed

### Client & research work (private repositories)

**Ebosi NEMT platform** — Non-emergency medical transport, architected and shipped end to end: two published iOS apps (rider + driver), Next.js admin dashboards, Node.js APIs, Stripe payments, and a PostgreSQL/Supabase backend. Scoped directly with the client, deployed to production, maintained under a support retainer.

**MDAMCR — automated multimodal data pipeline** *(Computational Biomedicine Lab, UH)* — A fully local AI pipeline (Whisper, LLaMA 3.2, LLaVA) automating transcription, entity extraction, and classification across 50+ case records. Evaluated output quality with B-cubed F1 and pairwise precision/recall.

---

## Background

**M.S. Engineering Data Science and AI** — University of Houston, Cullen College of Engineering · Aug 2025 – Dec 2026 (expected)
*Generative AI and Applications, Computer Vision, Applied Neural Networks, Machine Learning, Statistics for Data Science, LiDAR Systems*

**BSc (Hons) Computing** — University of Greenwich, London · 2019 – 2022

**Freelance Developer & Technical Consultant** — Ebosi Technologies / TMAC, University of Houston · Jul 2025 – May 2026
**Junior Developer** — uab bank, FinTech Digital & Card Dept., Yangon · Aug 2022 – Jun 2023
*Built and shipped digital payment apps (uabpay, pay+, SGH Plus) in React Native, integrated backend APIs, wrote automated tests, and debugged live production issues alongside product and security teams.*
**Web Developer Intern** — uab bank, Technology Dept., Yangon · Jun – Aug 2022

---

## Tech

**AI & automation** LangChain · LangGraph · agent orchestration & tool routing · RAG · prompt engineering · multimodal LLMs · Anthropic / OpenAI / DeepInfra APIs · FAISS · ChromaDB · Ollama · Hugging Face

**Languages** Python · TypeScript · JavaScript · SQL · C++ · PHP · Java

**Web & mobile** React · React Native · Next.js · Node.js · Expo · Laravel · Tailwind CSS

**Data & infra** PostgreSQL · MySQL · MongoDB · Supabase · Firebase · Docker · GitHub Actions · AWS · PySpark · scikit-learn · PyTorch

**Integrations** REST · GraphQL · OAuth 2.0 · webhooks · Stripe · Twilio

---

## What I'm looking for

Roles where I own an AI system end to end — agent and RAG pipelines that touch real business data, not demos. I'm most useful on the messy part: scoping an ambiguous process, finding the automatable pattern, and delivering the build independently.

Graduating **December 2026** and open to full-time AI/ML engineering, automation engineering, and applied AI roles.

## Reach me

[bhonekyawsihein.tech](https://bhonekyawsihein.tech) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/bhonekyawsihein) &nbsp;·&nbsp; [bhonekyawsihein@gmail.com](mailto:bhonekyawsihein@gmail.com)
