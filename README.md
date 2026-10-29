<div align="center">

# Awesome Agent Skills

### **Supercharge your AI coding agent with production-ready skills**

[![Skills](https://img.shields.io/badge/skills-7-blueviolet?style=for-the-badge)](#skills)
[![Tools](https://img.shields.io/badge/total_tools-100+-brightgreen?style=for-the-badge)](#skills)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](#license)
[![Platform](https://img.shields.io/badge/platform-Claude_Code_%7C_Codex_%7C_OpenClaw-orange?style=for-the-badge)](#compatibility)

<br />

A curated collection of open-source **agent skills** — modular capabilities that give AI coding agents real-world superpowers. From managing your entire financial life to creating AI-powered videos, each skill is battle-tested, well-documented, and ready to install.

**Built by [@6missedcalls](https://github.com/6missedcalls)**

<br />

[Get Started](#quick-start) · [Browse Skills](#skills) · [Contributing](#contributing)

---

</div>

## What Are Agent Skills?

Agent skills are **self-contained capability packages** that extend what AI coding agents can do. Each skill bundles:

- **SKILL.md** — Instructions the agent reads to understand when and how to use the skill
- **Scripts** — Executable automation (bash, Node.js, Python) the agent can invoke
- **References** — API docs, schemas, and domain knowledge loaded on-demand
- **Extensions** — Optional plugin modules with typed tools and configs

Think of them as **apps for your AI agent** — install one, and your agent gains an entirely new domain of expertise.

## Skills

### Finance & Trading

| Skill | Description | Tools | Links |
|:------|:------------|:-----:|:-----:|
| [**Personal Finance Skill**](#-personal-finance-skill) | Full-stack personal finance management — banking, investing, tax optimization, market intelligence, and social sentiment analysis | 75 | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/personal-finance-skill) |

### Video & Content Creation

| Skill | Description | Tools | Links |
|:------|:------------|:-----:|:-----:|
| [**Video Editing Skill**](#-video-editing-skill) | Trim, jump cut, caption (Hormozi/standard/minimal), text overlay, and speed change videos using FFmpeg + Whisper | 6 scripts | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/video-editing-skill) |
| [**Revid Skill**](#-revid-skill) | Revid API V2 automation for AI video creation, rendering, publishing, and media workflows | CLI wrapper | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/revid-skill) |

### Presentations & Docs

| Skill | Description | Tools | Links |
|:------|:------------|:-----:|:-----:|
| [**Slidev Multi-Agent Skill**](#-slidev-multi-agent-skill) | Create, theme, build, and export Slidev presentations using a script-first workflow with local references | 6 scripts | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/slidev-agent-skill) |

### Productivity & Integrations

| Skill | Description | Tools | Links |
|:------|:------------|:-----:|:-----:|
| [**Fireflies Skill**](#-fireflies-skill) | Search, summarize, and query Fireflies.ai meeting transcripts via GraphQL API | CLI wrapper | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/fireflies-skill) |
| [**ERPNext Skill**](#-erpnext-skill) | Comprehensive Frappe Framework & ERPNext v15 development reference with full API docs across 14+ modules | Reference | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/erpnext-skill) |
| [**SPECTER**](https://github.com/YannisKiefer/harvey-specter) | Negotiation preparation and relationship-aware drafts for difficult conversations | Markdown instructions | [Repo](https://github.com/YannisKiefer/harvey-specter) |

### Web & Protocols

| Skill | Description | Tools | Links |
|:------|:------------|:-----:|:-----:|
| [**WebMCP Skill**](#-webmcp-skill) | Interact with WebMCP-enabled websites via the W3C standard (Chrome 146+) — no DOM scraping, just structured JSON tools | Discovery + Invoke | [![GitHub](https://img.shields.io/badge/-Repo-181717?logo=github&logoColor=white)](https://github.com/6missedcalls/openclaw-webmcp-skill) |

---

## Skill Details

### 💰 Personal Finance Skill

> **75 tools across 7 extensions** for complete personal finance management

[![Repo](https://img.shields.io/badge/GitHub-personal--finance--skill-181717?logo=github)](https://github.com/6missedcalls/personal-finance-skill)

The most comprehensive agent skill in this collection. Connects to your real financial accounts and gives your AI agent the ability to monitor, analyze, and optimize your entire financial life.

**Architecture:**

```
Intelligence Layer
  tax-engine (23 tools)       — W-2/1099/K-1 parsing, liability calc, TLH, wash sales, AMT
  market-intel (10 tools)     — Finnhub, SEC EDGAR, FRED, BLS, Alpha Vantage
  social-sentiment (6 tools)  — StockTwits, X/Twitter, congressional trading

Data Source Adapters
  plaid-connect (8)    alpaca-trading (10)    ibkr-portfolio (9)

Foundation Layer
  finance-core (9 tools) — canonical models, storage, normalization, anomaly detection
```

**Key Capabilities:**
- **Banking** — Connect accounts via Plaid, sync transactions, track subscriptions, detect anomalies
- **Trading** — Place/cancel orders on Alpaca, monitor IBKR portfolios, track positions and P/L
- **Tax Engine** — Parse 15 IRS form types, estimate liability across 8 states, find tax-loss harvesting opportunities, check wash sale compliance
- **Market Intelligence** — Company news, SEC filings, analyst recommendations, FRED economic data, BLS labor stats
- **Social Sentiment** — StockTwits bull/bear scores, X/Twitter cashtag analysis, congressional trading disclosures
- **Guardrails** — Policy engine gates all side-effecting actions, approval-required for live trades

---

### ✂️ Video Editing Skill

> **6 Bash scripts** for local video editing powered by FFmpeg and Whisper

[![Repo](https://img.shields.io/badge/GitHub-video--editing--skill-181717?logo=github)](https://github.com/6missedcalls/video-editing-skill)

Edit videos with natural language — trim, remove silence, burn captions, add text overlays, and adjust speed. Pure Bash, zero runtime dependencies beyond FFmpeg and Whisper. Used and tested with OpenClaw.

**Key Capabilities:**
- **Trimming** — Cut to start/end timestamps with fast codec copy
- **Jump Cuts** — Auto-detect and remove silence with configurable thresholds
- **Captions** — Transcribe with Whisper, then burn in Hormozi, standard, or minimal style
- **Text Overlays** — Add positioned text at specific timestamps (7 positions)
- **Speed Changes** — Pitch-corrected playback speed adjustment
- **Pipeline** — Chain all operations in a single command via `edit.sh`

```bash
bash scripts/edit.sh video.mp4 \
  --jumpcut --caption --caption-style hormozi --speed 1.25
```

---

### 🎥 Revid Skill

> **Revid API V2 automation** for AI-powered video creation and publishing

[![Repo](https://img.shields.io/badge/GitHub-revid--skill-181717?logo=github)](https://github.com/6missedcalls/revid-skill)

Wraps the Revid.ai API into a clean script-first workflow. Handles render jobs, status polling, exports, publishing, media management, and consistent character workflows.

**Key Capabilities:**
- **Render Pipeline** — Submit render jobs from JSON payloads, poll status, download outputs
- **Script Wrapper** — `revid_api.sh` handles auth, endpoints, and common workflows
- **Reference-Driven** — Bundled API reference keeps agents accurate without burning context tokens

```bash
REVID_API_KEY=... bash scripts/revid_api.sh render payloads/render.json
REVID_API_KEY=... bash scripts/revid_api.sh status <project-id>
```

---

### 📊 Slidev Multi-Agent Skill

> **Script-first Slidev presentation workflow** across Claude Code, Codex, and OpenClaw

[![Repo](https://img.shields.io/badge/GitHub-slidev--agent--skill-181717?logo=github)](https://github.com/6missedcalls/slidev-agent-skill)

Gives your agent the ability to scaffold, author, theme, build, and export Slidev presentation decks with deterministic, repeatable scripts.

**Key Capabilities:**
- **Scaffold** — `slidev-init.sh` bootstraps a new deck
- **Author** — Core syntax, layout, and frontmatter references loaded on-demand
- **Theme** — Eject existing themes or scaffold new ones from scratch
- **Build & Export** — SPA builds and PDF/PNG exports via dedicated scripts
- **Cross-Platform** — Works identically across Claude Code, Codex, and OpenClaw

**Scripts:** `slidev-init.sh`, `slidev-dev.sh`, `slidev-build.sh`, `slidev-export.sh`, `slidev-theme-eject.sh`, `slidev-theme-scaffold.sh`

---

### 🔥 Fireflies Skill

> **Meeting intelligence** — search, summarize, and query transcripts via GraphQL

[![Repo](https://img.shields.io/badge/GitHub-fireflies--skill-181717?logo=github)](https://github.com/6missedcalls/fireflies-skill)

Connects your AI agent to Fireflies.ai so it can search across meeting transcripts, extract action items, generate summaries, and answer questions about past meetings.

**Key Capabilities:**
- **Search** — Find meetings by keyword, date range, or participant
- **Summarize** — Get AI-generated summaries and action items
- **AskFred** — Natural language Q&A against any transcript
- **CLI Wrapper** — `fireflies.sh` handles GraphQL translation and auth

```bash
./scripts/fireflies.sh transcripts --keyword "budget" --limit 10
./scripts/fireflies.sh askfred --query "What were the action items?" --transcript_id "ID"
```

---

### 🏭 ERPNext Skill

> **Complete Frappe Framework & ERPNext v15 development reference** for AI-assisted ERP development

[![Repo](https://img.shields.io/badge/GitHub-erpnext--skill-181717?logo=github)](https://github.com/6missedcalls/erpnext-skill)

Gives your agent full context on the Frappe Framework — DocTypes, controllers, hooks, REST APIs, form scripts, background jobs, and 14+ ERPNext module references. The agent can build complete Frappe apps from scratch.

**Reference Coverage:**
- **Core Framework** — Document API, Database API, Controllers, Hooks, REST API, Form Scripts, Testing
- **14+ Modules** — Accounting, Stock/Inventory, Manufacturing, CRM, HR & Payroll, and more
- **Patterns** — Common integration patterns, background job architecture, custom app scaffolding

---

### 🌐 WebMCP Skill

> **W3C WebMCP standard** — let agents interact with websites through structured tools, not DOM scraping

[![Repo](https://img.shields.io/badge/GitHub-openclaw--webmcp--skill-181717?logo=github)](https://github.com/6missedcalls/openclaw-webmcp-skill)

Built for the emerging WebMCP standard (Chrome 146+). Instead of brittle CSS selectors and DOM scraping, agents discover and invoke structured tools that websites explicitly register. JSON in, JSON out.

**Key Capabilities:**
- **Tool Discovery** — Enumerate tools registered by WebMCP-enabled sites
- **Structured Invocation** — Call tools with typed parameters, get structured responses
- **No Scraping** — Works through the site's declared API surface, not fragile DOM traversal

---

## Quick Start

### Claude Code

```bash
# Install any skill via Claude Code
claude install-skill https://github.com/6missedcalls/<skill-name>
```

### OpenClaw

```bash
# Install as an OpenClaw extension
openclaw install https://github.com/6missedcalls/<skill-name>
```

### Manual

```bash
# Clone and reference the SKILL.md in your agent config
git clone https://github.com/6missedcalls/<skill-name>
```

## Compatibility

| Platform | Supported |
|:---------|:---------:|
| Claude Code | Yes |
| OpenAI Codex | Yes |
| OpenClaw | Yes |
| Any SKILL.md-compatible agent | Yes |

## Contributing

Contributions welcome. If you'd like to add a skill to this list:

1. Fork this repository
2. Add your skill to the appropriate category in this README
3. Ensure your skill has a well-structured `SKILL.md`
4. Submit a pull request

## License

All skills in this collection are released under the [MIT License](LICENSE) unless otherwise noted.

---

<div align="center">

**Built with AI agents, for AI agents.**

[![GitHub](https://img.shields.io/badge/GitHub-@6missedcalls-181717?logo=github&logoColor=white&style=flat-square)](https://github.com/6missedcalls)

</div>
