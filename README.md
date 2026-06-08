<h1 align="center">Awais Tanveer Khan</h1>

<p align="center">
  <b>AI Engineer</b> · Production LLM Systems · Backend &amp; Infrastructure
</p>

<p align="center">
  <a href="mailto:awaistanveer206@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://www.linkedin.com/in/awaistanveerkhan/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://github.com/awaistanveerkhan"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
  <img src="https://img.shields.io/badge/+92--3360144300-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Phone"/>
  <img src="https://img.shields.io/badge/Islamabad,%20Pakistan-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location"/>
</p>

---

## About

AI engineer who ships **production LLM systems** and the backend and infrastructure behind them, for clients including **Mayo Clinic** and **Al Jazeera**. Builds agentic workflows (LangGraph, Claude Agent SDK), RAG, and document automation on top of extensive FastAPI services. Owns delivery end to end — from API design and async processing through Docker, CI/CD, and running servers on AWS/Azure.

---

## Experience

### Funavry Technologies — *AI Engineer*
<sub>Islamabad, Pakistan · Aug 2024 – Present</sub>

- Delivered production LLM systems end to end for enterprise and medical clients including **Mayo Clinic** and **Al Jazeera**, owning each project from API and retrieval through deployment and server operations on AWS/Azure.
- Designed RAG and semantic-search pipelines over large document corpora using **Qdrant** and **Azure AI Search** with hybrid retrieval, tuned chunking, and embeddings.
- Built multi-agent and agentic workflows with the **Claude Agent SDK** (reusable Agent Skills / `SKILL.md` modules) and **LangGraph**, replacing hand-wired graphs with reusable components and shortening agent development time.
- Designed and built the **FastAPI** backend across projects — REST API design, authentication, and async ingestion/task processing with **Celery + Redis**, serving thousands of documents per project under concurrent load.
- Built and maintained **GitHub Actions** CI/CD pipelines for frontend and backend (Docker) across test, staging, and production, cutting release time from **10 min → 2 min** with near-zero-downtime deploys.
- Provisioned and managed AWS/Azure servers end to end — environment configuration, **Nginx** reverse proxy and SSL/TLS, and database administration.
- Stood up **LLM evaluation** against human-labeled gold sets to track screening, retrieval, and extraction quality across releases, and served as the engineering point of contact in **Mayo Clinic** client meetings.

---

## Projects

### LISRMA — Living Evidence Synthesis Platform for Systematic Reviews
<sub>**Client:** Mayo Clinic</sub>
<br/>
<sub>`Claude Agent SDK` · `LangGraph` · `RAG` · `Qdrant` · `FastAPI` · `MySQL` · `Redis` · `Celery` · `OpenAI` · `Docker` · `GitHub Actions` · `Nginx` · `AWS EC2` · `S3`</sub>

- Reached **~93%** screening agreement with human reviewers on a held-out sample, by building a multi-agent LLM workflow (Agent Skills via the Claude Agent SDK) over title/abstract pairs.
- Built RAG retrieval with Qdrant, hybrid search, and tuned chunking/embeddings over research papers to improve recall on relevant studies.
- Raised field-level extraction accuracy to **~90%**, by building multi-agent structured-extraction pipelines (LangGraph) with human-in-the-loop validation.
- Owned the deployment pipeline end to end — separate dev and prod environments on dedicated AWS EC2 VMs, each with its own database, deployed through a GitHub Actions pipeline that targeted the correct environment automatically.
- Configured per-server Nginx reverse proxies for frontend and backend, restricting staging domains to whitelisted URL paths while keeping public domains openly accessible.

### Guideline — Version Control &amp; Publishing System for LISRMA
<sub>**Client:** Mayo Clinic</sub>
<br/>
<sub>`FastAPI` · `MySQL` · `SQLAlchemy` · `Redis` · `Celery` · `GitHub Actions`</sub>

- Eliminated manual versioning errors and cut time-to-publish in half, by building a biweekly automated **draft → staging → release** workflow with full rollback support.
- Reduced editor effort from hours to minutes per update, by building a drag-and-drop admin layout composer for guideline authoring with AI suggestions.
- Kept public page loads fast under traffic, by implementing snapshot-based rendering with Redis caching behind an Nginx reverse proxy with rate limiting.

### TAX GENII — Retrieval-Augmented Chatbot for Australian Tax Law
<sub>`Azure AI Search` · `Flask` · `SQLAlchemy` · `SQL` · `Python`</sub>

- Made **200k+** tax-law documents queryable in natural language, by building a RAG chatbot with Azure AI Search using semantic + vector retrieval.
- Kept multi-turn legal queries responsive, by designing a modular Flask backend and APIs for scalable query handling.

### Persona Clone — Multi-Platform Digital Persona Engine
<sub>`RAG` · `Azure OpenAI` · `Azure AI Search` · `ElevenLabs` · `FastAPI` · `MySQL`</sub>

- Built lifelike, continuously updated digital personas across multiple platforms, by ingesting WhatsApp/TikTok/Instagram data into a multi-LLM RAG framework with cron-based knowledge-base enrichment.
- Enabled real-time voice conversations at **~20** concurrent sessions, by integrating ElevenLabs voice cloning and deploying on Azure VMs with Azure OpenAI and AI Search.
- Configured the single test environment end to end — server, database, and the acidbase.io domain — for rapid development iteration.

### Al Jazeera Finance Chatbot — AI-Powered Conversational Financial Assistant
<sub>**Client:** Al Jazeera</sub>
<br/>
<sub>`LLMs` · `RAG` · `JSON Knowledge Base` · `Python` · `FastAPI` · `MySQL`</sub>

- Resolved the majority of financial queries without escalation, by engineering nested JSON-based question flows with an LLM fallback layer that preserves full conversational context.
- Delivered context-aware multi-turn conversations over Al Jazeera content, by combining a retrieval system with conversational memory for hybrid structured + generative responses.

### Synnc — Collaboration Platform for LinkedIn Influencers and Brands
<sub>`FastAPI` · `Firebase` · `OpenAI API` · `MongoDB` · `Docker` · `Render` · `S3`</sub>

- Enabled end-to-end campaign lifecycle management for brands and influencers, by building RESTful APIs for task delegation and scheduling with Firebase auth and custom multi-tenant RBAC.
- Cut manual content-drafting time by **~60%**, by integrating OpenAI GPT for AI-assisted copywriting within the campaign workflow.

---

## Education

### National University of Modern Languages (NUML)
<sub>Islamabad, Pakistan · Sep 2020 – Jul 2024</sub>
<br/>
**B.S. Computer Science**

> **Thesis — GammaLogger:** Sensor-based Side-channel Attack Detection via Text and Image Inference

- Reached **93% keystroke prediction accuracy**, by building a smartphone sensor app that demonstrates keystroke-inference side-channel attacks via multi-modal sensor fusion.
- Reconstructed typed sentences from passive sensor data, by modeling keystroke events as text and image inference problems.

---

## Skills

**AI / LLM Systems**
<br/>
![Claude Agent SDK](https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=flat-square&logo=anthropic&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![RAG](https://img.shields.io/badge/RAG_Pipelines-5A4FCF?style=flat-square)
![Prompt Engineering](https://img.shields.io/badge/Prompt_Engineering-412991?style=flat-square&logo=openai&logoColor=white)
![Semantic Search](https://img.shields.io/badge/Semantic_Search-0F9D58?style=flat-square)
![Embeddings](https://img.shields.io/badge/Embeddings-FF6F00?style=flat-square)
![LLM Eval](https://img.shields.io/badge/LLM_Evaluation-6A1B9A?style=flat-square)

**Information Retrieval**
<br/>
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white)
![Azure AI Search](https://img.shields.io/badge/Azure_AI_Search-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Hybrid Search](https://img.shields.io/badge/Hybrid_Search-2E7D32?style=flat-square)
![Chunking](https://img.shields.io/badge/Document_Chunking-455A64?style=flat-square)
![Indexing](https://img.shields.io/badge/Large--scale_Indexing-37474F?style=flat-square)

**Backend**
<br/>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![REST](https://img.shields.io/badge/REST_API_Design-005571?style=flat-square)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Cloud &amp; DevOps**
<br/>
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Databases &amp; Storage**
<br/>
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square&logo=pinecone&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white)

**Languages &amp; Tools**
<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

<p align="center"><sub>Open to AI engineering roles · Let's build something.</sub></p>
