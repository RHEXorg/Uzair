<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0a,50:1a1a1a,100:2a2a2a&height=200&section=header&text=Uzair%20&fontSize=60&fontColor=ffffff&fontAlignY=38&desc=Engineering%20autonomous%20AI%20systems%20%C2%B7%20automation%20%C2%B7%20full-stack&descAlignY=62&descSize=14&animation=fadeIn" width="100%"/>

<br/>

<a href="https://rehxa.com">
  <img src="https://img.shields.io/badge/Currently_Building-RehXa-000000?style=for-the-badge&labelColor=000000"/>
</a>
<a href="https://www.linkedin.com/in/uzair-farooq-7968b2312/">
  <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="mailto:rhexorg@gmail.com">
  <img src="https://img.shields.io/badge/Email-Reach_Out-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>
<a href="https://rhex.netlify.app/">
  <img src="https://img.shields.io/badge/Portfolio-Live-1a1a1a?style=for-the-badge"/>
</a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=3500&pause=800&color=ffffff&center=true&vCenter=true&width=720&lines=Engineering+the+boring+work+out+of+business.;AI+agents+%C2%B7+automation+%C2%B7+full-stack+systems.;Production-first.+Built+to+ship%2C+scale%2C+survive.;Quietly+replacing+manual+work+with+code." alt="Typing intro" />

</div>

<br/>

---

## About

Engineer working across **AI, automation, and full-stack development** — the kind who notices the manual process everyone's quietly tolerating and quietly replaces it with code.

My work spans backend systems, AI integrations, automation pipelines, web and mobile interfaces, and the data architecture that holds them together. Less interested in shortcuts, more interested in figuring out what a system *should* look like before writing the first line.

The interesting engineering challenge isn't making the AI work — it's making it know when *not to*.

<br/>

<table>
<tr>
<td align="center" width="33%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40"/>
<br/><b>Production Systems</b>
<br/><sub>SaaS platforms running for real users</sub>
</td>
<td align="center" width="33%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" width="40"/>
<br/><b>Applied AI</b>
<br/><sub>RAG · agents · multi-tenant inference</sub>
</td>
<td align="center" width="33%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" width="40"/>
<br/><b>Full Stack</b>
<br/><sub>Backend · web · mobile · data</sub>
</td>
</tr>
</table>

---

## Currently Shipping — RehXa

> **An autonomous AI agent that handles WhatsApp & Email for businesses, 24/7.**
> [rehxa.com](https://rehxa.com)

A multi-tenant B2B SaaS platform that ingests business knowledge, connects to customer messaging channels, and deploys AI agents that reply with full conversational context, brand-accurate tone, and confidence-gated escalation.

<details>
<summary><b>🏗️ &nbsp; Architecture & Engineering Decisions</b></summary>

<br/>

| Layer | Stack | Why |
|---|---|---|
| **API** | FastAPI (Python 3.11+) | Async-first, Pydantic validation, OpenAPI by default |
| **Database** | Supabase Postgres + pgvector | Row-level multi-tenant isolation by `org_id`; vector search co-located with relational data |
| **Background Jobs** | Celery + Redis | Knowledge ingestion, embedding generation, follow-up scheduling — never blocks the request path |
| **AI Inference** | OpenAI (primary) + Anthropic Claude (fallback) | Provider-redundant; per-org system prompts; confidence scoring on every response |
| **OAuth & Email** | Composio | Bypasses 6-week Google OAuth verification; unified Gmail / Outlook surface |
| **WhatsApp** | Meta Cloud API (Embedded Signup) | Per-org access tokens; webhook-driven ingestion |
| **Billing** | Lemon Squeezy | Merchant-of-record; handles global VAT and trials |
| **Frontend** | Next.js 14 App Router · Tailwind · shadcn/ui | Server components for dashboard, edge runtime for marketing |

**Engineering principles applied:**
- Strict per-org data isolation enforced at the **query layer**, not just the API layer
- All long-running operations offloaded to Celery — request path stays fast
- Confidence-gated AI: every response carries a 0.0–1.0 score, sub-threshold replies escalate to a human
- Pre-launch security audit completed; load tested with Locust at 50 concurrent users sustained

</details>

<details>
<summary><b>⚡ &nbsp; Live System Capabilities</b></summary>

<br/>

- Unified inbox across WhatsApp + Email with real-time conversation threading
- RAG over uploaded business documents (up to 500MB per tenant)
- Per-tenant tone and personality calibration from sample writing
- Automatic multilingual handling — language detected from inbound message
- Follow-up engine running on cron-driven Celery beat
- Team accounts with role-based assignment
- GDPR-compliant data export and deletion

</details>

<br/>

<div align="center">
<a href="https://rehxa.com"><img src="https://img.shields.io/badge/▶_View_Live_Product-000000?style=for-the-badge&labelColor=000000"/></a>
&nbsp;
<a href="https://www.linkedin.com/in/uzair-farooq-7968b2312/"><img src="https://img.shields.io/badge/💬_Talk_About_It-1a1a1a?style=for-the-badge&labelColor=1a1a1a"/></a>
</div>

> *Source code is private. Architecture documentation and a video walkthrough available on request.*

---

## Selected Work

### Production Software

<table>
<tr>
<td width="50%" valign="top">

**[RehXa](https://rehxa.com)** — *Live*

Multi-tenant AI customer-message platform. Reads, classifies, and replies to Gmail & WhatsApp messages 24/7 — grounded in the customer's own knowledge base.

`FastAPI` `Supabase` `pgvector` `Celery` `Next.js` `Composio` `WhatsApp Cloud API`

</td>
<td width="50%" valign="top">

**[DevScope](https://github.com/RHEXorg)**

AI developer assistant — debugging, doc generation, and OCR-driven context capture for codebases that need to be understood quickly.

`OpenRouter` `OCR` `Tailwind`

</td>
</tr>
</table>

### Applied AI Tooling

| Project | What it does |
|---|---|
| **Excel AI Insights** | Tabular ingestion → automated summarization & chart generation |
| **Resume Optimizer** | Embedding-based JD-to-resume alignment scoring |
| **YouTube Summarizer** | Transcript chunking, chapter generation, semantic compression |
| **Website Chatbot** | Site-scoped RAG with custom embeddings |
| **Feedback Analyzer** | Review clustering, pain-point extraction, sentiment trends |

### Mobile Engineering

| App | Surface area |
|---|---|
| **Habity** | Habit tracking — streaks, 2FA, cloud sync, in-app help center |
| **MoneyMate** | Real-time FX conversion across 150+ currencies |
| **OilHub** | Pakistan-first engine oil marketplace (UI prototype) |

---

## Engineering Stack

<div align="center">

#### Languages
<p>
  <img src="https://skillicons.dev/icons?i=python,typescript,javascript,cpp,c"/>
</p>

#### Backend & Data
<p>
  <img src="https://skillicons.dev/icons?i=fastapi,nodejs,postgres,supabase,redis,docker"/>
</p>

#### Frontend & Mobile
<p>
  <img src="https://skillicons.dev/icons?i=nextjs,react,tailwind,vite,expo"/>
</p>

#### AI & Infra
<p>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/Anthropic-191919?style=flat-square"/>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
  <img src="https://img.shields.io/badge/pgvector-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white"/>
  <img src="https://img.shields.io/badge/Composio-7B61FF?style=flat-square"/>
</p>

#### Deployment & Ops
<p>
  <img src="https://skillicons.dev/icons?i=vercel,cloudflare,railway,git,github"/>
</p>

</div>

---

## Inside the Workshop

<div align="center">

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/dynamic/json?label=Repositories&query=public_repos&url=https%3A%2F%2Fapi.github.com%2Forgs%2FRHEXorg&style=for-the-badge&color=0d1117&labelColor=000000&logo=github"/>
<br/><sub>Active codebases</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Stack-Python_%C2%B7_TS_%C2%B7_C%2B%2B-0d1117?style=for-the-badge&labelColor=000000"/>
<br/><sub>Primary languages</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Focus-AI_%C2%B7_SaaS_%C2%B7_Mobile-0d1117?style=for-the-badge&labelColor=000000"/>
<br/><sub>Engineering surface</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Status-Shipping-22c55e?style=for-the-badge&labelColor=000000"/>
<br/><sub>Always</sub>
</td>
</tr>
</table>

<br/>

### Pinned Work

<a href="https://github.com/RHEXorg/R.H.E.X.">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=RHEXorg&repo=R.H.E.X.&hide_border=true&title_color=ffffff&icon_color=ffffff&text_color=c9d1d9&bg_color=0d1117"/>
</a>

<br/><br/>

### What I Build, In One Picture

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1a1a1a', 'primaryTextColor':'#ffffff', 'primaryBorderColor':'#3a3a3a', 'lineColor':'#6a6a6a', 'fontSize':'14px'}}}%%
flowchart LR
    A[Customer Message] --> B[FastAPI Gateway]
    B --> C{Classifier}
    C -->|High confidence| D[RAG Retrieval]
    C -->|Low confidence| E[Human Escalation]
    D --> F[LLM Inference<br/>OpenAI · Claude]
    F --> G[Tone Layer]
    G --> H[Reply Sent]
    H --> I[(Postgres + pgvector)]
    E --> I
    I --> J[Follow-up Engine<br/>Celery + Redis]
    J --> A

    style A fill:#1a1a1a,stroke:#3a3a3a,color:#fff
    style B fill:#1a1a1a,stroke:#3a3a3a,color:#fff
    style C fill:#2a2a2a,stroke:#4a4a4a,color:#fff
    style D fill:#1a1a1a,stroke:#3a3a3a,color:#fff
    style E fill:#7c2d12,stroke:#9a3412,color:#fff
    style F fill:#1e1b4b,stroke:#3730a3,color:#fff
    style G fill:#1a1a1a,stroke:#3a3a3a,color:#fff
    style H fill:#14532d,stroke:#166534,color:#fff
    style I fill:#0c4a6e,stroke:#075985,color:#fff
    style J fill:#1a1a1a,stroke:#3a3a3a,color:#fff
```

<sub>The RehXa pipeline — simplified.</sub>

</div>

---

## How I Work

<table>
<tr>
<td width="50%" valign="top">

#### 🎯 &nbsp; Production-first
Every system is built to ship, scale, and survive real users. No demos, no toy code.

#### 🔒 &nbsp; Security on day one
Pre-launch audits, RLS, encryption at rest and in transit — not afterthoughts.

</td>
<td width="50%" valign="top">

#### 📊 &nbsp; Observability by default
Structured logging, load testing, error budgets. If it runs, it's measured.

#### ✂️ &nbsp; Lean architecture
No premature abstraction. No frameworks chosen for résumé reasons.

</td>
</tr>
</table>

---

## Open to Conversations About

- **Production AI systems** — RAG pipelines, agentic workflows, LLM cost optimization
- **Multi-tenant SaaS architecture** — from schema design to billing integration
- **Mobile applications** — React Native, App Store & Play Store delivery
- **Engineering roles** where the work is technical, the standards are high, and the impact is real

<br/>

<div align="center">

<a href="mailto:rhexorg@gmail.com">
  <img src="https://img.shields.io/badge/Start_a_Conversation-000000?style=for-the-badge&logo=maildotru&logoColor=white"/>
</a>
&nbsp;
<a href="https://www.linkedin.com/in/uzair-farooq-7968b2312/">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
&nbsp;
<a href="https://rehxa.com">
  <img src="https://img.shields.io/badge/Visit_RehXa-1a1a1a?style=for-the-badge"/>
</a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2a2a2a,50:1a1a1a,100:0a0a0a&height=100&section=footer" width="100%"/>

<sub>Engineering teams ship products. I do both.</sub>

</div>
