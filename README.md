 <div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0a,100:1a1a1a&height=180&section=header&text=R.H.
  E.X.&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=Applied%20AI%20%C2%B7%20Distributed%20Systems%20%C2%B7%20Production%
  20Software&descAlignY=62&descSize=14" width="100%"/>

  <br/>

  <p>
    <a href="https://rehxa.com"><img 
  src="https://img.shields.io/badge/Flagship-RehXa.com-000000?style=flat-square&labelColor=000000"/></a>
    <a href="https://www.linkedin.com/in/uzair-farooq-7968b2312/"><img 
  src="https://img.shields.io/badge/LinkedIn-Profile-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
    <a href="mailto:rhexorg@gmail.com"><img 
  src="https://img.shields.io/badge/Contact-Email-D14836?style=flat-square&logo=gmail&logoColor=white"/></a>
    <a href="https://rhex.netlify.app/"><img 
  src="https://img.shields.io/badge/Portfolio-Live-1a1a1a?style=flat-square"/></a>
  </p>

  <br/>

  <table>
  <tr>
  <td align="center" width="33%">
  <b>Production Systems</b><br/>
  <sub>SaaS platforms serving real customers</sub>
  </td>
  <td align="center" width="33%">
  <b>Applied AI</b><br/>
  <sub>LLM pipelines, RAG, multi-tenant inference</sub>
  </td>
  <td align="center" width="33%">
  <b>Full Stack</b><br/>
  <sub>FastAPI · Next.js · Supabase · Celery</sub>
  </td>
  </tr>
  </table>

  </div>

  ---

  ## About

  We design and ship production-grade software where **applied AI meets real-world business operations**. Our work spans
  distributed backends, vector retrieval pipelines, secure multi-tenant SaaS, and high-fidelity mobile clients.

  We are not interested in demos. We ship.

  ---

  ## Flagship — RehXa

  > **An autonomous AI agent that handles WhatsApp & Email for small and medium businesses, 24/7.**
  > [rehxa.com](https://rehxa.com)

  RehXa is a multi-tenant B2B SaaS platform that ingests business knowledge (RAG), connects to customer messaging channels,
   and deploys AI agents capable of replying with full conversational context, brand-accurate tone, and confidence-gated
  escalation.

  <details>
  <summary><b>Architecture & Engineering Decisions</b></summary>

  <br/>

  | Layer | Stack | Rationale |
  |---|---|---|
  | API | FastAPI (Python 3.11+) | Async-first, Pydantic validation, OpenAPI by default |
  | Database | Supabase Postgres + pgvector | Row-level multi-tenant isolation by `org_id`; vector search co-located with
  relational data |
  | Background Jobs | Celery + Redis | Knowledge ingestion, embedding generation, follow-up scheduling — never blocks the
  request path |
  | AI Inference | OpenAI (primary) + Anthropic Claude (fallback) | Provider-redundant; per-org system prompts; confidence
  scoring on every response |
  | OAuth & Email | Composio | Bypasses 6-week Google OAuth verification cycle; unified Gmail / Outlook surface |
  | WhatsApp | Meta Cloud API (Embedded Signup) | Per-org access tokens; webhook-driven ingestion |
  | Billing | Lemon Squeezy | Merchant-of-record; handles global VAT and trials |
  | Frontend | Next.js 14 App Router · Tailwind · shadcn/ui | Server components for dashboard, edge runtime for marketing |

  **Engineering principles applied:**
  - Strict per-org data isolation enforced at the query layer, not just the API layer
  - All long-running operations (document ingestion, batch follow-ups) offloaded to Celery
  - Confidence-gated AI: every response carries a 0.0–1.0 score, sub-threshold replies escalate to a human
  - Pre-launch security audit completed; load tested with Locust (50 concurrent users sustained)

  </details>

  <details>
  <summary><b>Live System Capabilities</b></summary>

  <br/>

  - Unified inbox across WhatsApp + Email with real-time conversation threading
  - RAG over uploaded business documents (up to 500MB per tenant)
  - Per-tenant tone and personality calibration from sample writing
  - Automatic multilingual handling (language detected from inbound message)
  - Follow-up engine running on cron-driven Celery beat
  - Team accounts with role-based assignment
  - GDPR-compliant data export and deletion

  </details>

  <div align="center">
  <a href="https://rehxa.com"><img 
  src="https://img.shields.io/badge/▶_View_Live_Product-000000?style=for-the-badge&labelColor=000000"/></a>
  &nbsp;
  <a href="#"><img 
  src="https://img.shields.io/badge/📐_Architecture_Docs-1a1a1a?style=for-the-badge&labelColor=1a1a1a"/></a>
  </div>

  > Source code is private. Architecture documentation, system design diagrams, and a video walkthrough are available in
  the linked architecture repo.

  ---

  ## Selected Work

  ### Production Software

  <table>
  <tr>
  <td width="50%" valign="top">

  **[RehXa](https://rehxa.com)** — *Live*
  Multi-tenant AI customer-message platform.
  `FastAPI` `Supabase` `pgvector` `Celery` `Next.js` `Composio` `WhatsApp Cloud API`

  </td>
  <td width="50%" valign="top">

  **[DevScope](https://github.com/Qrf2/Devscope)**
  AI developer assistant — debugging, doc generation, OCR-driven context capture.
  `OpenRouter` `OCR` `Tailwind`

  </td>
  </tr>
  </table>

  ### Applied AI Tooling

  | Project | Surface Area |
  |---|---|
  | **Excel AI Insights** | Tabular ingestion → automated summarization & chart generation |
  | **Resume Optimizer** | Embedding-based JD-to-resume alignment scoring |
  | **YouTube Summarizer** | Transcript chunking, chapter generation, semantic compression |
  | **Website Chatbot** | Site-scoped RAG with custom embeddings |
  | **Feedback Analyzer** | Review clustering, pain-point extraction, sentiment trend analysis |

  ### Mobile Engineering

  | App | Surface Area |
  |---|---|
  | **Habity** | Habit tracking — streaks, 2FA, cloud sync, in-app help center |
  | **MoneyMate** | Real-time FX conversion across 150+ currencies |
  | **OilHub** | UI prototype — Pakistan-first engine oil marketplace |

  ---

  ## Engineering Stack

  <p align="left">
    <img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white"/>
    <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
    <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
    <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
    <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
  </p>

  <p align="left">
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
    <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white"/>
    <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
    <img src="https://img.shields.io/badge/pgvector-000000?style=flat-square"/>
    <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white"/>
  </p>

  <p align="left">
    <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"/>
    <img src="https://img.shields.io/badge/Anthropic_Claude-191919?style=flat-square"/>
    <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
    <img src="https://img.shields.io/badge/Composio-7B61FF?style=flat-square"/>
  </p>

  <p align="left">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
    <img src="https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white"/>
    <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/>
    <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white"/>
    <img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white"/>
  </p>

  ---

  ## How We Work

  - **Production-first.** Every project is built to ship, scale, and survive real users.
  - **Security on day one.** Pre-launch audits, RLS, encryption at rest and in transit — not as afterthoughts.
  - **Observability by default.** Structured logging, load testing, error budgets.
  - **Lean architecture.** No premature abstraction. No frameworks chosen for résumé reasons.

  ---

  ## Engagement

  We work with founders, engineering teams, and organizations on:

  - Production AI systems — RAG pipelines, agentic workflows, LLM cost optimization
  - Multi-tenant SaaS architecture — from schema design to billing integration
  - Mobile applications — React Native, App Store / Play Store delivery
  - Technical due diligence — architecture review for investors and acquirers

  <p align="left">
    <a href="mailto:rhexorg@gmail.com"><img 
  src="https://img.shields.io/badge/Start_a_Conversation-000000?style=for-the-badge&logo=maildotru&logoColor=white"/></a>
    <a href="https://www.linkedin.com/in/uzair-farooq-7968b2312/"><img 
  src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
    <a href="https://rehxa.com"><img src="https://img.shields.io/badge/Visit_RehXa-1a1a1a?style=for-the-badge"/></a>
  </p>

  ---

  <div align="center">
  <sub>R.H.E.X. — Engineering teams ship products. We do both.</sub>
  </div>
