# Uzair Farooq

**AI Engineer · Mobile Developer · Founder, [RehXa](https://rehxa.com)**

<p>
  <a href="https://www.linkedin.com/in/uzair-qrf-815ba026a/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>&nbsp;
  <a href="https://uzairqrf.netlify.app/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=flat&logo=vercel&logoColor=white" alt="Portfolio"/>
  </a>&nbsp;
  <a href="mailto:uzairqrf@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white" alt="Email"/>
  </a>&nbsp;
  <a href="https://rehxa.com" target="_blank">
    <img src="https://img.shields.io/badge/RehXa-rehxa.com-0066FF?style=flat" alt="RehXa"/>
  </a>
</p>

I build production-grade AI systems and cross-platform mobile applications. My work focuses on applied LLM integration, intelligent automation pipelines, and shipping software that solves real business problems.

---

### RehXa — AI-Powered Customer Communication Platform

> **[rehxa.com](https://rehxa.com)** — Your business never misses a customer message again.

RehXa is an autonomous AI communication layer for businesses. It processes incoming WhatsApp and Email messages in real time, understands customer intent, generates contextually accurate replies from a per-business knowledge base, and escalates to humans only when confidence is low.

<details>
<summary><b>Architecture & Capabilities</b></summary>
<br>

**How it works:**

```
Customer Message (WhatsApp / Email)
        │
        ▼
  Webhook Layer ─────── 360dialog / Composio
        │
        ▼
  Tenant Router ─────── Supabase (business identification)
        │
        ▼
  Context Assembly ──── Knowledge Base + History + RAG
        │
        ▼
  LLM Engine ────────── Claude API (intent + response)
        │
        ▼
  Confidence Gate
  ├── ≥ 0.85 → Auto-send
  └── < 0.85 → Draft → Owner review → Approve/Edit
        │
        ▼
  Delivery ──────────── 360dialog / Composio
        │
        ▼
  Analytics ─────────── Supabase + Next.js Dashboard
```

**Key capabilities:**
- Real-time message processing via 360dialog (WhatsApp) and Composio (Email/Calendar)
- Per-business RAG pipeline — documents, pricing, policies, tone calibration
- Confidence-scored responses with automatic escalation logic
- Automated follow-up engine for lead nurturing and customer retention
- Unified inbox with team routing and conversation analytics
- Multi-language support with automatic detection

**Stack:** Node.js · Claude API · Supabase · Next.js · Composio · 360dialog · Railway

</details>

---

### Selected Projects

| Project | Description | Stack |
|---|---|---|
| [DevScope](https://github.com/Qrf2/Devscope) | AI developer assistant — code debugging, analysis, and documentation generation | OCR · GPT · OpenRouter · Tailwind |
| Habity | Habit tracker with streaks, 2FA, cloud sync, and integrated help center | React Native · Expo · Firebase |
| Excel AI Insights | Spreadsheet analysis — upload data, receive AI-generated summaries and chart recommendations | Python · Streamlit · GPT |
| Resume Optimizer | AI-driven resume-to-job-description matching and optimization engine | Python · GPT · Streamlit |

---

### Technical Skills

```
AI & LLMs          Claude API · OpenAI GPT · DeepSeek · OpenRouter · RAG · Prompt Engineering · LangChain
Mobile              React Native · Expo · Redux Toolkit · NativeWind
Backend             Node.js · Python · Supabase · Firebase · REST APIs · Stripe
Frontend            Next.js · TypeScript · JavaScript · Tailwind CSS
Data                Pandas · Scikit-learn · Web Scraping · PDF/Excel Processing
Infrastructure      Railway · Linux · Git · Arduino/IoT
```

---

### Currently

- Scaling RehXa toward public launch and first 100 paying customers
- Building integrations: Google Calendar, Stripe, Shopify via Composio
- Advancing work with LangChain and production RAG architectures
- Exploring IoT and hardware-software integration

---

### GitHub Activity

<p>
  <img src="https://github-readme-stats.vercel.app/api?username=qrf2&show_icons=true&theme=default&hide_border=true&count_private=true" alt="GitHub Stats" />
</p>

---

### Contact

Open to collaboration on AI-powered products, mobile applications, and automation systems.

<p>
  <a href="mailto:uzairqrf@gmail.com"><b>Email</b></a> · 
  <a href="https://www.linkedin.com/in/uzair-qrf-815ba026a/"><b>LinkedIn</b></a> · 
  <a href="https://uzairqrf.netlify.app/"><b>Portfolio</b></a> · 
  <a href="https://rehxa.com"><b>RehXa</b></a>
</p>
