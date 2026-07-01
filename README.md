# 🤖 AI Agent Team — OpenCode Agent Definitions & Custom Skills

> Personal agent team for OpenCode AI editor.
> Created by **Mike** (Chayapol Promsavana) for daily dev workflow.

## 🧠 Agents

| Agent | Role | File |
|-------|------|------|
| **steward** 🏆 | Default — pragmatic, automation-first, system-minded | `agents/steward.md` |
| **frontend** 🎨 | UX/UI, product design, visual system, CSS motion | `agents/frontend.md` |
| **backend** ⚙️ | API, database, architecture, backend systems (v2.0) | `agents/backend.md` |
| **debugger** 🐛 | System detective, bug hunter, architecture analyst | `agents/debugger.md` |
| **scribe** 📝 | Documentation, Thai Open Source textbooks, Obsidian notes | `agents/scribe.md` |
| **minecrafter** ⛏️ | AI Minecraft player — Brain-Body architecture | `agents/minecrafter.md` |

### Architecture Pattern — Hybrid Lean Core + On-Demand Skills

> มาตรฐานการออกแบบ Agent ดูที่ [`docs/agent-design-standard.md`](docs/agent-design-standard.md)

Each agent follows a **lean core + on-demand skills** pattern:
- **Agent file (core)**: identity, principles, core skills list, tools, environment (~30-120 lines)
- **Skills** (on-demand): deep domain knowledge loaded only when needed (~40-80 lines each)

Benefits: **55-85% token savings** vs monolithic agent files, easier to maintain, trivial to extend.

## 📦 Custom Skills (11 skills)

Skills created/designed by me (not third-party). Located in `skills/`:

### Design

| Skill | Description |
|-------|-------------|
| `design-image-composer` | Smart image integration — search Pexels/Pixabay, compose, attribute |
| `design-thinking` | UX thinking framework — problem framing, 10-step process, task analysis |
| `design-screen-spec` | 17-point screen specification standard |
| `design-quality` | Design quality rubric (0-100), review checklist, anti-patterns |
| `design-output` | 5 output formats — screen, polish, HTML, motion, image |

### Backend

| Skill | Description |
|-------|-------------|
| `backend-architecture` | System design — SoC, 3-Layer, Plugin System, Design Patterns |
| `backend-api-design` | API standards — RESTful, versioning, error handling, validation |
| `backend-database` | Database — schema design, indexing, query optimization, migration |

### Reference

| Skill | Description |
|-------|-------------|
| `open-design-resources` | Bridge to Open Design ecosystem (175+ skills, 151 design systems) |
| `opensource-textbook` | Generate Thai-language textbooks from open source repos (v7.2) |
| `aetox-astro` | Aetox AI architecture, automation, and enterprise web systems |

## 🤖 ZCode Agents

แยกจาก OpenCode agents — สำหรับใช้ใน **ZCode ADE** (`~/.zcode/agents/`):

| Agent | Role | File |
|-------|------|------|
| **backend** ⚙️ | Backend systems architecture (Chinese) | `zcode-agents/backend.md` |
| **frontend** 🎨 | UI/UX, visual system, mobile design (English) | `zcode-agents/frontend.md` |

ZCode agents มีขนาดเล็กกว่า OpenCode version (~50 บรรทัด) เพราะ ZCode import skills แบบ manual (`$skill-name`) และมี Guardrails/Self-Review อยู่ใน environment ของ ZCode เอง

## 🔧 Local Setup

### OpenCode Agents
Agent files go in: `%USERPROFILE%\.config\opencode\agents\`
Skills go in: `%USERPROFILE%\.agents\skills\<name>\SKILL.md`

### ZCode Agents
Agent files go in: `~/.zcode/agents/`
Skills import: Settings → Skills → Import จาก `.agents/skills/`

### Environment Dependencies

- **Windows 11** + PowerShell 7 + WSL2 Ubuntu
- **OpenCode** with MCP servers: Gmail, Obsidian, Sequential Thinking, Speak TTS, Windows MCP, Image Resolver, Pixabay, Exa, Context7
- **ZCode** (v3.2.1+, port 12345): ADE by Zhipu AI, uses DeepSeek V4 Pro/Flash as custom provider
- **Image MCPs**: Image Resolver (Pexels 200 req/hr), Pixabay (5000 req/hr)
- **Export**: `E:\Web-html\` for HTML prototypes
- **Obsidian vault**: `E:\MikeData`
- **Open Design**: `E:\GitHup\opensource\open-design` (v0.11.1)

## 📁 Repo Structure

```
ai-agent-team/
├── agents/          # Agent definitions — lean core (opencode format)
├── zcode-agents/    # Agent definitions — ZCode ADE format (leaner)
├── skills/          # Custom skills — on-demand (SKILL.md per directory)
├── docs/            # Architecture & design standards
│   └── agent-design-standard.md   ← มาตรฐานการออกแบบ Agent
├── README.md
└── .gitignore
```

---

*Last updated: 1 Jul 2026 (+ ZCode agents, mobile skills)*
