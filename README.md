# Vitalii Bogachev

**Senior AI Engineer — LLM, RAG, MCP.** Tbilisi, Georgia · open to remote.

I build LLM products that run in production, not demos. Since 2024 I have
built and operated **BookahTranslate**, a paid AI document-translation SaaS,
and helped product teams adopt RAG, custom MCP servers and AI coding agents.

My foundation is 13 years of engineering: full-stack TypeScript/Node.js and
Python on high-load fintech and SaaS platforms — an institutional crypto
exchange, a US solar SaaS where I was Team Lead — and a start in QA
automation. That is why my AI systems ship with evals, regression gates,
observability and provider fallback.

---

### Open source

Tools that came out of the production work, each with a write-up that
includes what went wrong along the way.

| Repository | What it does and what it found |
|---|---|
| **[pr-witness](https://github.com/talhayme/pr-witness)** | Runs the *base branch's* tests against a pull request's code — the run CI never does — and shows each rewritten test with its old and new assertion. CLI, GitHub Action with signed evidence, Claude Code plugin; on PyPI. Evaluated on real coding-agent commits with the tool frozen and the labels committed first, misses published with the hits. [Write-up](https://talhayme.github.io/blog/3355-agent-test-edits/) |
| **[ftgate](https://github.com/talhayme/ftgate)** | Checks that a fine-tuned small model is served the bytes it was trained on. Measured what a known Ollama bug costs — the tool schema reaches the model as a Go struct dump, and Qwen2.5-0.5B's exact-argument rate drops from 39/40 to 31/40 ([ollama#14601](https://github.com/ollama/ollama/issues/14601)) — and found a pre-fix chat template still embedded in Qwen's official GGUFs ([Qwen3#1921](https://github.com/QwenLM/Qwen3/issues/1921)). Its dataset linter shows 43.5% of rows in hermes-function-calling-v1's two `func_calling` configs losing the answer at `max_seq_len=2048`. On PyPI. [Write-up](https://talhayme.github.io/blog/six-tool-calling-datasets/) |
| **[lora-glossary](https://github.com/talhayme/lora-glossary)** | A 0.5B model fine-tuned on a laptop in 160 seconds for glossary-consistent legal translation: adherence 10.5% → 94.7% (18 of 19 held-out prompts), against GPT-4o-mini's 68.4% on the same prompts. |

---

### Smaller demos

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
