# 🤖 AI Agent Team — OpenCode Agent Definitions & Custom Skills

> Personal agent team for OpenCode AI editor.
> Created by **Mike** (Chayapol Promsavana) for daily dev workflow.

## 🧠 Agents

| Agent | Role | File |
|-------|------|------|
| **steward** 🏆 | Default — pragmatic, automation-first, system-minded | `agents/steward.md` |
| **designer** 🎨 | UX/UI, product design, visual system, CSS motion | `agents/designer.md` |
| **backend** ⚙️ | API, database, architecture, backend systems | `agents/backend.md` |
| **debugger** 🐛 | System detective, bug hunter, architecture analyst | `agents/debugger.md` |
| **scribe** 📝 | Documentation, Thai Open Source textbooks, Obsidian notes | `agents/scribe.md` |
| **minecrafter** ⛏️ | AI Minecraft player — Brain-Body architecture | `agents/minecrafter.md` |

### Architecture Pattern — Hybrid Lean Core + On-Demand Skills

> มาตรฐานการออกแบบ Agent ดูที่ [`docs/agent-design-standard.md`](docs/agent-design-standard.md)

Each agent follows a **lean core + on-demand skills** pattern:
- **Agent file (core)**: identity, principles, core skills list, tools, environment (~30-120 lines)
- **Skills** (on-demand): deep domain knowledge loaded only when needed (~40-80 lines each)

Benefits: **55-85% token savings** vs monolithic agent files, easier to maintain, trivial to extend.

## 📦 Custom Skills

Skills created/designed by me (not third-party). Located in `skills/`:

### Design

| Skill | Description |
|-------|-------------|
| `design-image-composer` | Smart image integration — search Pexels/Pixabay, compose, attribute |
| `design-thinking` | UX thinking framework — problem framing, 10-step process, task analysis |
| `design-screen-spec` | 17-point screen specification standard |
| `design-quality` | Design quality rubric (0-100), review checklist, anti-patterns |
| `design-output` | 5 output formats — screen, polish, HTML, motion, image |

### Reference

| Skill | Description |
|-------|-------------|
| `open-design-resources` | Bridge to Open Design ecosystem (175+ skills, 151 design systems) |
| `opensource-textbook` | Generate Thai-language textbooks from open source repos (v7.2) |
| `aetox-astro` | Aetox AI architecture, automation, and enterprise web systems |

## 🔧 Local Setup

These agents run in **OpenCode** (`C:\Users\Gigabyte\.config\opencode\`).

Agent files go in: `%USERPROFILE%\.config\opencode\agents\`
Skills go in: `%USERPROFILE%\.agents\skills\<name>\SKILL.md`

### Environment Dependencies

- **Windows 11** + PowerShell 7 + WSL2 Ubuntu
- **OpenCode** with MCP servers: Gmail, Obsidian, Sequential Thinking, Mineflayer Bot, Speak TTS, Windows MCP, Image Resolver, Pixabay, Firecrawl, Exa, Context7
- **Image MCPs**: Image Resolver (Pexels 200 req/hr), Pixabay (5000 req/hr)
- **Export**: `E:\Web-html\` for HTML prototypes
- **Obsidian vault**: `E:\MikeData`
- **Open Design**: `E:\GitHup\opensource\open-design` (v0.11.1)

## 📁 Repo Structure

```
ai-agent-team/
├── agents/        # Agent definitions — lean core (opencode format)
├── skills/        # Custom skills — on-demand (SKILL.md per directory)
├── docs/          # Architecture & design standards
│   └── agent-design-standard.md   ← มาตรฐานการออกแบบ Agent
├── README.md
└── .gitignore
```

---

*Last updated: 29 Jun 2026*
