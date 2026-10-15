<h1 align="center">Awais Tanveer Khan</h1>

<p align="center">
  <b>AI Engineer · Full-Stack</b><br/>
  Agentic systems, retrieval, and the production products built around them
</p>

<p align="center">
  <a href="mailto:awaistanveer206@gmail.com"><img src="https://img.shields.io/badge/Email-awaistanveer206%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://www.linkedin.com/in/awaistanveerkhan/"><img src="https://img.shields.io/badge/LinkedIn-awaistanveerkhan-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <img src="https://img.shields.io/badge/Based%20in-Islamabad%2C%20Pakistan-555555?style=flat-square&logo=googlemaps&logoColor=white" alt="Location"/>
</p>

---

I build AI products end to end: the agent or retrieval layer, the API and data model underneath it, the interface people use, and the infrastructure it runs on. Since 2024 I have shipped production LLM systems for **Mayo Clinic**, **Al Jazeera** and **LodgeiT**, usually owning the work from first requirements call to deployment.

On Mayo Clinic's LISR platform I lead the client meetings myself, from gathering feature requirements and proposing improvements to building and refining what we agree on.

### Focus areas

- **Agentic systems** — multi-agent orchestration on the Claude Agent SDK and LangGraph, MCP servers, human-in-the-loop review
- **Grounded retrieval** — RAG with citation integrity, hybrid and graph-expanded search, confidence-aware answers
- **Product engineering** — React / Next.js frontends, FastAPI services, real-time collaboration, payments
- **Production delivery** — Docker, GitHub Actions CI/CD, AWS and Azure (including AKS), LLM tracing and evaluation

---

### Experience

**Funavry** · Islamabad · Aug 2024 – present

| Role | Period |
|---|---|
| AI Engineer | Aug 2026 – present |
| Associate AI Engineer | Nov 2024 – Jul 2026 |
| AI Trainee Engineer | Aug 2024 – Oct 2024 |

Client delivery across healthcare research (Mayo Clinic), media (Al Jazeera) and tax advisory (LodgeiT).

---

### Selected work

#### Mayo Clinic · LISR — Living Evidence Synthesis Platform

A platform for running systematic reviews of clinical evidence and keeping them current as new studies appear. I work across the AI layer, the product and the deployment.

**AI screening and agentic extraction**
`Claude Agent SDK` `MCP` `OpenAI` `Anthropic` `FastAPI` `Celery` `Redis`

- Reached **~93% screening agreement** with human reviewers across **28k+ studies** using multi-agent workflows built on Agent Skills.
- Extraction orchestrator dispatches five specialist agents, each with its own skill file and MCP server. Work fans out in bounded parallel chunks, so one failed chunk never sinks the run. Field-level accuracy reaches **~90%** with human-in-the-loop validation.
- Every extracted value is stored alongside the verbatim source text it came from, so reviewers verify a single cell instead of rereading the paper.
- Production MCP server (FastMCP, 23 tools, token auth) that lets Claude Code and Codex operate real review projects under each user's own permissions.
- AI reviewers sit on the team like humans, with per-stage approval switches and human corrections stored beside the AI's original decision.

**Collaborative manuscript editor**
`Next.js` `FastAPI` `Redis` `SSE`

- Google Docs-style editor where charts and tables come straight from live analysis data and are frozen as versioned snapshots, with a field-by-field diff when the data changes.
- Invertible audit log covering text, structure, tables and references; track changes that also revert table edits and citation numbering.
- Live presence over Redis pub/sub-backed SSE streams. Optimistic locking refuses a colliding save rather than silently overwriting it.

**Living guidelines and publishing engine**
`FastAPI` `Next.js` `MySQL` `SQLAlchemy` `Celery`

- Turned static reviews into self-updating guidelines with a fortnightly automated draft → staging → published cycle and full rollback, guarded by Redis locks and idempotency checks.
- Published pages are frozen as immutable, citable snapshots. Large datasets are snapshotted into indexed tables, so the public site still filters and paginates thousands of records.
- New evidence is diffed deterministically between versions, then an LLM writes the plain-language summary.

**Deployment** — isolated dev and prod environments on dedicated EC2 VMs, environment-aware GitHub Actions pipelines, per-server Nginx and SSL.

Architecture notes: [AI screening & extraction](https://claude.ai/artifact/GT6KEdM1KCenHszJdGbFiR) · [Manuscript editor](https://claude.ai/artifact/DArzKxLHasr3BzUutdPiEZ) · [Guidelines & publishing](https://claude.ai/artifact/1EH6XrqL1KAncFnnLeyQvY)

#### TaxGenii — AI advisory for Australian tax, migration and superannuation

Built for LodgeiT.
`LangGraph` `Azure AI Search` `Neo4j` `Azure OpenAI` `Celery` `LangSmith`

- Made **200k+ tax-law documents** queryable in natural language. LangGraph routes intent and splits complex questions into parallel sub-questions; semantic retrieval is expanded through a Neo4j legal citation graph.
- Users only see the sources the model actually used, and low retrieval confidence makes the model hedge instead of guess.
- Analyst → Critic → Judge agent pipeline for high-stakes answers. Provider-agnostic, with bring-your-own-key for OpenAI, Gemini, Anthropic and Grok.
- One pipeline exposed three ways: web app, REST API and a 7-tool MCP server. JWT with revocation, OIDC SSO, and per-user document isolation enforced inside the search index.

Architecture notes: [TaxGenii](https://claude.ai/artifact/WKLXKQSc5dUARiG1nWFJyz)

#### Synnc — Brand × LinkedIn creator marketplace

`FastAPI` `MongoDB` `React` `Stripe` `Azure OpenAI` `AKS`

- Two-sided platform with 172 API routes covering discovery, campaigns, deliverables, payments, messaging and analytics, plus Nia, an AI assistant that turns a brief into a live campaign.
- Fraud-resistant reporting: a vision model reads the creator's analytics screenshot and the server rejects any claim more than 5% off.
- Stripe subscriptions for brands and Stripe Connect payouts for creators, with payment state changed only by signature-verified webhooks.
- Zero-downtime rolling deploys to Azure Kubernetes Service through GitHub Actions with SHA-pinned images.

Architecture notes: [Synnc](https://claude.ai/artifact/2aj3PDz6cWnwxafrike1Cw)

#### Markdown Studio — prototype to production

`React` `TypeScript` `Web Workers` `IndexedDB`

- Rebuilt an approved single-file mockup for production in 10 days, keeping every pixel of the signed-off design.
- Found and closed 4 working script-injection exploits with layered sanitisation and a per-request CSP, proven against a 13-case attack corpus.
- 1,499 unit tests and 363 end-to-end tests across Chrome, Firefox and Safari, with zero accessibility violations.

Architecture notes: [Markdown Studio](https://claude.ai/artifact/PkSZHBaGBJVimBeFRV5mhY)

#### Also shipped

- **Al Jazeera — Finance chatbot** · structured JSON question flows with an LLM fallback that keeps full conversational context; resolves most financial queries without escalation.
- **Persona Clone** · RAG-grounded, in-character replies over ingested social data, spoken back in a cloned voice (ElevenLabs) across ~20 concurrent real-time sessions on Azure.
- **Mayo Clinic — BeaconLab** · designed and built solo: public site for an oncology-AI research lab plus the admin platform behind it.

---

### Tech stack

| Area | Tools |
|---|---|
| **AI / LLM** | Claude Agent SDK, LangGraph, LangChain, MCP (FastMCP), OpenAI, Anthropic, Azure OpenAI, LangSmith, prompt engineering, LLM evaluation |
| **Retrieval** | Qdrant, Azure AI Search, Pinecone, FAISS, Neo4j, hybrid search, embeddings, Docling, LlamaParse |
| **Backend** | Python, FastAPI, Flask, Celery, Redis, REST, SSE, WebSockets |
| **Frontend** | React, Next.js, TypeScript, Tailwind CSS, React Native |
| **Data** | PostgreSQL, MySQL, MongoDB, Firebase, SQLAlchemy |
| **Cloud & DevOps** | AWS, Azure, AKS, Docker, Nginx, GitHub Actions |
| **Payments** | Stripe (subscriptions, Connect, webhooks) |

---

### Education

**B.S. Computer Science** — National University of Modern Languages (NUML), Islamabad · 2020 – 2024
Thesis: *GammaLogger*, sensor-based side-channel keystroke inference combining text and image modelling, reaching **93%** keystroke-prediction accuracy.

---

<p align="center">
  Open to full-stack AI roles and freelance engagements · <a href="mailto:awaistanveer206@gmail.com">awaistanveer206@gmail.com</a>
</p>
