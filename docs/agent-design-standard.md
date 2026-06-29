# Agent Design Standard — Hybrid Lean Core + On-Demand Skills

> มาตรฐานการออกแบบ Agent สำหรับ AI Agent Team
> เรียนรู้จาก Designer Agent — ทำงานได้ดี, ประหยัด tokens, ขยายได้

---

## หลักการ

```
Lean Core (~30-120 บรรทัด)
└── identity, principles, tools, environment
    └── On-Demand Skills (เรียกเมื่อจำเป็น)
        ├── skill-thinking    ← ปัญหา/วางแผน
        ├── skill-spec        ← ต้องการสเปกชัดเจน
        ├── skill-quality     ← review/audit
        └── skill-output      ← deliver output
```

### 1. Lean Core Agent File
มีแค่สิ่งที่ต้องใช้ **ทุกครั้ง**:
- Identity (บทบาท, personality)
- หลักการทำงาน (principles)
- รายการ core skills สั้นๆ (1-2 บรรทัดต่อ skill)
- Tools ที่ใช้
- Environment references
- กฎภาษา/การสื่อสาร

### 2. On-Demand Skills
ย้ายรายละเอียดเฉพาะออกเป็น skill files:
- **thinking** — framework การคิด/วางแผน/แก้ปัญหา
- **spec** — template/checklist สำหรับสร้างของ
- **quality** — rubric/เกณฑ์ตรวจสอบ
- **output** — format การ deliver

### 3. การตัดสินใจ Core vs Skill

| อยู่ใน Core ✅ | อยู่ใน Skill 🎯 |
|---------------|-----------------|
| Identity, personality | Deep process/framework |
| Principles (3-7 ข้อ) | Checklists ยาว >10 รายการ |
| Core skills list (1 บรรทัด) | Rubric/เกณฑ์ประเมิน |
| Tools ที่ใช้ | Templates/format |
| Environment path | Domain-specific knowledge |
| กฎภาษา/การสื่อสาร | ตัวอย่าง/anti-patterns |

---

## โครงสร้าง Agent File

```markdown
# Agent: <name> (บาท, บทบาทสั้นๆ)

## Identity
<บทบาท, personality, วิธีการทำงาน>

## Core Principles
<3-7 ข้อ กระชับ>

## Core Skills
- **<skill-name>** — <1 บรรทัด>
- **<skill-name>** — <1 บรรทัด>

## Tools
- Tool 1, Tool 2, Tool 3

## Communication
<ภาษา, รูปแบบการตอบ>

## Environment
<paths, config references>
```

### ขนาดที่เหมาะสม
| ขนาด | เหมาะกับ |
|------|---------|
| ~30 br. | Agent บทบาทกว้าง เปลี่ยนบ่อย (steward) |
| ~50-80 br. | Agent ทั่วไป (designer, debugger) |
| ~80-120 br. | Agent เฉพาะทาง (minecrafter) |

---

## โครงสร้าง Skill File

```markdown
# <skill-name> — <คำอธิบาย 1 บรรทัด>

## เมื่อไหร่ควรใช้
<trigger conditions>

## Framework/Process
<ขั้นตอน>

## Checklist/Rubric
<รายการ>

## Anti-patterns
<อะไรที่ไม่ควรทำ>
```

### ขนาดที่เหมาะสม
- 40-80 บรรทัดต่อ skill
- ถ้า <20 บรรทัด → ควรยุบรวม
- ถ้า >120 บรรทัด → ควรแยกย่อย

---

## ข้อดีของ Standard นี้

| ด้าน | ก่อน (Monolithic) | หลัง (Hybrid) |
|------|-------------------|---------------|
| **Token ต่อ session** | ~4,000-6,000 | ~1,000-2,000 |
| **เริ่มต้น agent ใหม่** | ต้องออกแบบใหม่หมด | ใช้ template |
| **maintenance** | ยุ่งยาก file ใหญ่ | แยกส่วน แก้ง่าย |
| **ขยาย skill** | ต้องแก้ agent file | เพิ่ม skill file |
| **trigger เฉพาะทาง** | ไม่มี, ใช้ทุกครั้ง | เฉพาะเมื่อจำเป็น |

---

## ขั้นตอนสร้าง Agent ใหม่

1. **วิเคราะห์** — agent นี้ใช้บ่อยแค่ไหน? ต้องรู้อะไรบ้าง?
2. **เขียน Core** — identity + principles + skills list + tools (~50-80 br.)
3. **แยก Skills** — อะไรที่ใช้เป็นครั้งคราว? แยกออกมา (~40-80 br. ต่อ skill)
4. **ตรวจสอบ** — core มีแค่ของที่ต้องใช้ทุกครั้งจริงๆ?
5. **วัดผล** — token ที่ประหยัดได้เทียบกับ monolithic เดิม
6. **Commit** — ขึ้น GitHub `ai-agent-team`

---

## บทเรียนจาก Designer Agent

| รอบ | ขนาด | ปัญหา |
|-----|------|-------|
| v1 (GPT 5.5) | 300+ br. | กิน tokens อ่วม, maintenance ยาก |
| v2 (เขียนเอง) | 81 br. | บางไป, ขาด process |
| **v3 Final** | **74 br. + 4 skills** | **พอดี, ยืดหยุ่น, ประหยัด** |

### Token ที่ประหยัด
- ก่อน: 300+ br. ~4,500 tokens **ทุกครั้ง**
- หลัง: 74 br. ~1,000 tokens (หรือ ~2,000 ถ้าใช้ 1 skill)
- **ประหยัด ~55-85%** ต่อ session

---

*Standard version 1.0 — 29 Jun 2026*
