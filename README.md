# Vitalii Bogachev

**Senior AI Engineer — LLM, RAG, MCP.** Tbilisi, Georgia · open to remote.

I build LLM products that run in production, not demos. Since 2024 I have
built and operated **BookahTranslate**, a paid AI document-translation SaaS,
and helped product teams adopt RAG, custom MCP servers and AI coding agents.

My foundation is 6+ years of full-stack TypeScript/Node.js and Python on
high-load fintech and SaaS platforms — an institutional crypto exchange, a US
solar SaaS where I was Team Lead — plus a QA-automation background. That is
why my AI systems ship with evals, regression gates, observability and
provider fallback.

---

### Open demos

Three standalone repositories, each extracted from a pattern I use in
production work. All run **offline** — no API key, no network — so they can
be cloned and executed in under a minute.

| Repository | What it shows |
|---|---|
| **[llm-eval-harness](https://github.com/talhayme/llm-eval-harness)** | Golden-set evaluation with a CI release gate: groundedness and hallucination metrics, absolute thresholds, per-case regression detection. CI asserts the gate rejects a known-bad run. |
| **[mcp-toolserver](https://github.com/talhayme/mcp-toolserver)** | An MCP server built properly: strict JSON schemas, errors written for the model to act on, and a calculator sandboxed against code execution with four independent layers. |
| **[rag-grounded](https://github.com/talhayme/rag-grounded)** | A RAG pipeline that refuses rather than guesses: calibrated confidence floors, hybrid dense + lexical retrieval, citations carrying source and heading. |

Each has a test suite (84–92% coverage) and green CI. Their known weaknesses
are pinned as tests, not hidden.

---

### What I work with

**LLM & AI** — OpenAI API (GPT-4), Anthropic Claude API, RAG, embeddings,
vector databases, semantic search, MCP servers & tool calling, LLM
evaluation, prompt regression testing, LLM observability, prompt-injection
testing, inference cost optimization, Claude Code · Codex · Cursor

**Languages** — Python, TypeScript, JavaScript

**Backend** — Node.js (NestJS, Express), FastAPI, Flask, Django/DRF, Celery,
REST, GraphQL (Apollo), WebSocket, OAuth 2.0

**Data** — PostgreSQL, MongoDB, MySQL, Redis, SQLAlchemy

**Infra & QA** — Docker, Kubernetes, AWS, GitLab CI, Jenkins, Nginx, Linux,
Prometheus, Grafana, pytest, Playwright, Cypress

---

### Selected production work

**BookahTranslate** — AI document-translation SaaS, in production with paying
subscribers. End-to-end LLM pipeline on GPT-4 and Claude: parsing, chunking,
context assembly, translation, document reassembly. Handles PDF, EPUB and
DOCX up to 300+ pages while preserving layout. Automatic fallback between
providers and models; every prompt or model change gated behind an evaluation
set with 80+ tests.

**AI implementation consulting** — RAG over corporate knowledge bases, custom
MCP servers connecting LLMs to internal tools, and rolling out AI coding
agents into engineering workflows with quality gates before release.

---

📄 [Portfolio](https://talhayme.github.io/portfolio-vitalii) ·
✉️ bogachev.vitaliy91test@gmail.com ·
💬 [Telegram](https://t.me/tenkuioo)
