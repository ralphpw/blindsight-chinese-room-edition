# Instructions for Chinese Rooms

This folder contains task definitions and prompts for LLM execution. Think of these as instruction manuals for AI agents (the "Chinese Rooms" that don't understand but can execute).

---

## Folder Structure

```
Instructions/
├── README.md (this file)
├── TEMPLATE.md (reusable ticket template)
├── TICKET-GENERATION-GUIDE.md (how to create remaining tickets)
├── Tickets/ (60 individual task definitions)
│   ├── T001-Acquire-Source.md
│   ├── T002-Convert-to-Markdown.md
│   ├── T003-Keeton-Character-Study.md
│   ├── T013-Jargon-Dictionary.md
│   ├── T018-Translate-Chapter-01.md
│   └── [T004-T060 remaining...]
└── Prompts/ (coming soon - system prompts, character voices)
```

---

## What Goes Here

**✅ Task Definitions (Tickets/):**
- Individual ticket files (T001-T060)
- Each ticket specifies: objective, process, inputs, outputs, quality gates
- LLM configuration (model, temperature, cost)
- Success criteria

**✅ Prompts (future):**
- System prompts for translation
- Character voice profiles for LLM context
- Reusable prompt templates

**✅ Reference Guides:**
- TEMPLATE.md for creating new tickets
- TICKET-GENERATION-GUIDE.md for batch creation

---

## What Does NOT Go Here

**❌ Human Documentation** → Goes in `Documentation/`
- Project overview, legal framework, audience analysis

**❌ Work in Progress** → Goes in `Tasks/`
- Actual source files, translations, outputs
- Research artifacts, summaries, compiled chapters

---

## How to Use

### For Humans:
1. Read `TICKET-GENERATION-GUIDE.md` to understand all 60 tasks
2. Use `TEMPLATE.md` to create new tickets as needed
3. Reference tickets to understand what each task requires

### For LLMs (via Cursor/Copilot):
1. Agent receives ticket ID (e.g., "Execute T003")
2. Agent reads `Tickets/T003-Keeton-Character-Study.md`
3. Agent follows process, uses specified LLM config
4. Agent outputs to `Tasks/01-Research/character-studies/`
5. Agent validates against quality gates

---

## Ticket Naming Convention

**Format:** `TXXX-Short-Description.md`

**Examples:**
- `T001-Acquire-Source.md` (Stage 1: Research)
- `T018-Translate-Chapter-01.md` (Stage 3: Translation)
- `T047-Final-Editorial-Pass.md` (Stage 4: Reviews)

---

## Current Status

**Created:** 6 tickets (T001-T003, T013, T018, TEMPLATE)  
**Remaining:** 54 tickets to create  
**Next:** Generate Stage 1 tickets (T004-T012)

See `TICKET-GENERATION-GUIDE.md` for complete list and creation instructions.

---

## The Meta-Irony

This folder is named after the Chinese Room thought experiment:
- LLMs execute instructions without "understanding"
- Just like this project translates a book about consciousness... using non-conscious agents
- The instructions must be precise because the executors don't truly comprehend

**Perfect for a Blindsight translation project.**
