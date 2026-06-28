---
name: aetox-astro
description: Aetox AI architecture, automation, and enterprise web systems. Use when the user mentions "Aetox", "Aetox Astro", "Aetox CLI", or asks about their own company/brand. Covers the Aetox CLI tool, desktop app, web services, and knowledge about the founder and company.
---

# Aetox Astro

**"The Closing Engine: สถาปัตยกรรมที่เปลี่ยนความซับซ้อนให้เป็นการตัดสินใจ"**

Aetox คือบริษัทเทคโนโลยีไทยที่ออกแบบระบบ AI, ระบบอัตโนมัติ, และระบบเว็บระดับองค์กร

## Ecosystem Overview

| Component | Path |
|-----------|------|
| CLI | `E:\Aetox\Aetox-cli\aetox.exe` |
| Desktop App | `C:\Users\Gigabyte\AppData\Local\Programs\Aetox Astro\Aetox Astro.exe` |
| Web Source | `E:\Aetox\Aetox_web` |
| CLI Source | `E:\Aetox\Aetox-cli` |
| Business Docs | `E:\Aetox\Aetox_web\docs\` |

## Company & Brand

- **Founder:** Chayapol Promsavana (Mike / ไมค์) — National AI Gold Medalist
- **Vision:** ผู้นำด้าน AI Architecture และระบบอัตโนมัติระดับองค์กร
- **Style:** Elite Minimalism — Powerful, Concise, Authoritative
- **Core Values:** Architectural Excellence, ROI-Driven Engineering, Data Sovereignty

### Target Market

- **Startups** — foundation ที่ scale ได้ตั้งแต่วันแรก
- **SMEs** — ลดต้นทุนด้วย Automation
- **Enterprises** — เปลี่ยนผ่านสู่ AI โดยไม่เสียความปลอดภัย

## Aetox CLI

Go-based coding agent CLI (`aetox.exe`) ที่ทำงานเป็น autonomous coding agent ได้

### Usage

```powershell
aetox [flags] [goal...]
aetox chat "goal"       # run one shot and exit
aetox                    # interactive mode
```

### Sample Commands

```powershell
# One-shot mode (uses full-access approval)
& "E:\Aetox\Aetox-cli\aetox.exe" "fix the bug in main.go"

# Interactive mode
& "E:\Aetox\Aetox-cli\aetox.exe"

# With specific model
& "E:\Aetox\Aetox-cli\aetox.exe" --model-provider openai --model-name gpt-4o "refactor this module"

# With debug logging
& "E:\Aetox\Aetox-cli\aetox.exe" --debug --debug-log C:\temp\aetox.log "help"
```

### Supported Providers

cohere, deepseek, gemini, groq, lmstudio, mistral, noop, ollama, openai, openrouter, perplexity, together

### Built-in CLI Skills

When aetox CLI runs, it has these built-in skills available: fs (file system), write, read, shell, git, githubRepoSummary, delete, echo, time, help, list

## Products & Services

### 1. AI Agent & RAG (สถาปัตยกรรมเอเจนต์อัจฉริยะ)
- Hybrid Retrieval (PDF, Excel, Docx + external APIs)
- Strategic Reasoning
- Source Referencing 100%

### 2. Workflow Automation (ระบบอัตโนมัติอัจฉริยะ)
- Data Pipeline Integration (ERP, CRM, Spreadsheet)
- Automated Processing (billing, lead screening, sales)
- Error Detection & Alerting

### 3. Enterprise Web Systems (ระบบเว็บระดับองค์กร)
- High-Performance Architecture (Edge Network)
- Real-time KPI Dashboards
- Role-Based Access Control (RBAC)

### Implementation Path
1. Discovery — วิเคราะห์รอยรั่วในธุรกิจ
2. Architecting — ออกแบบ Blueprint
3. Engineering — พัฒนาและทดสอบ
4. Optimization — ปรับจูนต่อเนื่อง

## Aetox Astro Desktop App

Desktop Electron app (Python FastAPI backend + Next.js frontend) สำหรับนำเสนอบริการ

```powershell
# Launch desktop app
& "C:\Users\Gigabyte\AppData\Local\Programs\Aetox Astro\Aetox Astro.exe"
```

## Infrastructure & Tech Stack

- **CLI:** Go (Golang)
- **Desktop:** Electron + Python FastAPI + Next.js
- **Web:** Next.js (i18n: th/en), Tailwind CSS, Framer Motion
- **Backend:** Python, SQLAlchemy, Swiss Ephemeris, MongoDB (Mongoose)
- **Monorepo:** `E:\Aetox\` includes CLI, web, skills, Discord bot, docstruct
- **CI:** docs at `E:\Aetox\aetox-skills\`, `E:\Aetox\aetox-discord-setup\`

## Architecture Notes

- The CLI at `E:\Aetox\Aetox-cli\aetox.exe` is a complete autonomous agent — it has its own thinking, tool execution, and model switching capability
- The desktop app resources live at `C:\Users\Gigabyte\AppData\Local\Programs\Aetox Astro\resources\` with `app.asar`, `backend\backend.exe` (Python), and `frontend-out\` (Next.js static)
- For the web app dev loop: use `npm run dev` in `E:\Aetox\Aetox_web`
