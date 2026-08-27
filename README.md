# Bhone Kyaw Si Hein

**AI & automation engineer with production full-stack experience.**
I turn manual business processes into working automated systems — LLM agents and orchestration layers built on top of real enterprise data, shipped end to end.

📍 Houston, TX &nbsp;·&nbsp; 🎓 M.S. Engineering Data Science & AI, University of Houston (Dec 2026) &nbsp;·&nbsp; 💼 **Open to AI / ML engineering and automation roles**

---

## What I do

**Build LLM agents that do real work.** LangChain / LangGraph orchestration, tool routing, RAG pipelines, multimodal calls. The interesting part isn't the prompt — it's designing tool boundaries and fallback paths so the agent *fails explicitly* instead of hallucinating when a tool returns nothing usable.

**Wire AI into enterprise systems.** REST/GraphQL, OAuth 2.0, webhooks, API gateways. I've replaced a recurring manual export process at an enterprise client with an automated ERP extraction pipeline over the NetSuite REST API — SuiteQL queries, OAuth 2.0 auth, and monthly chunking to work around record-count limits.

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

### Client & research work (private repositories)

**Ebosi NEMT platform** — Non-emergency medical transport, architected and shipped end to end: two published iOS apps (rider + driver), Next.js admin dashboards, Node.js APIs, Stripe payments, and a PostgreSQL/Supabase backend. Scoped directly with the client, deployed to production, maintained under a support retainer.

**Automated ERP data extraction pipeline** — Replaced a recurring manual export for an enterprise client. SuiteQL over the NetSuite REST API with OAuth 2.0, webhooks, and monthly chunking to stay under record-count limits. Also scoped ERP migration and compliance workstreams (Odoo, NetSuite, CMMC) by mapping how the client's operations actually ran, then converting that into a phased technical roadmap.

**MDAMCR — automated multimodal data pipeline** *(Computational Biomedicine Lab, UH)* — A fully local AI pipeline (Whisper, LLaMA 3.2, LLaVA) automating transcription, entity extraction, and classification across 50+ case records. Evaluated output quality with B-cubed F1 and pairwise precision/recall.

**Spatial Omics Copilot** *(research team of 6 engineers)* — Owned the LangGraph orchestration layer of a RAG chatbot that lets researchers query spatial transcriptomics data in plain English: tool definitions, routing between vector retrieval / live dataset queries / image-based answers, and multimodal prompt construction served via DeepInfra.

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

**Integrations** REST · GraphQL · OAuth 2.0 · webhooks · NetSuite (SuiteQL / REST) · Odoo · Stripe · Twilio

---

## What I'm looking for

Roles where I own an AI system end to end — agent and RAG pipelines that touch real business data, not demos. I'm most useful on the messy part: scoping an ambiguous process, finding the automatable pattern, and delivering the build independently.

Graduating **December 2026** and open to full-time AI/ML engineering, automation engineering, and applied AI roles.

## Reach me

[LinkedIn](https://www.linkedin.com/in/bhonekyawsihein) &nbsp;·&nbsp; [bhonekyawsihein@gmail.com](mailto:bhonekyawsihein@gmail.com)
