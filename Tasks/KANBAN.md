# Blindsight: The Sarasti Translation - Project Kanban

**Project Start:** TBD  
**Target Completion:** 6-9 months from start  
**Current Phase:** Planning

---

## Overview

This Kanban board tracks all tasks across 5 sequential stages. Each ticket has a dedicated file in `01-Documentation/Tickets/`.

**Stages:**
1. **Research** - Deep analysis and data extraction
2. **Summaries** - Story context and character states
3. **Translation** - Chapter-by-chapter translation
4. **Illustrations** - Visual documentation (100-ticket range)
5. **Reviews** - Quality validation
6. **Publication** - Final formats and distribution

---

## Status Legend

- ⏳ **TODO** - Not started
- 🔄 **IN PROGRESS** - Currently being worked on
- ⏸️ **BLOCKED** - Waiting on dependencies
- ✅ **REVIEW** - Awaiting validation
- ✓ **DONE** - Completed and validated

---

## Task Status Board

### **Stage 1: Research (Foundation)**

| ID | Task | Status | LLM | Limit | Req'd | Cost | Started | Done |
|----|------|--------|-----|-------|-------|------|---------|------|
| T001 | Acquire source material | ⏳ TODO | Human | - | - | $0 | - | - |
| T002 | Convert to Markdown (22 chapters) | ⏳ TODO | Human/Script | - | - | $0 | - | - |
| T003 | Keeton character study | ⏳ TODO | Opus 4.1 | 200K | 15K | $3 | - | - |
| T004 | Sarasti character study | ⏳ TODO | Opus 4.1 | 200K | 15K | $3 | - | - |
| T005 | Szpindel character study | ⏳ TODO | Opus 4.1 | 200K | 15K | $3 | - | - |
| T006 | Bates character study | ⏳ TODO | Opus 4.1 | 200K | 15K | $3 | - | - |
| T007 | Cunningham character study | ⏳ TODO | Opus 4.1 | 200K | 15K | $3 | - | - |
| T008 | Extract Keeton dialogue | ⏳ TODO | Sonnet 3.5 | 200K | 10K | $1 | - | - |
| T009 | Extract Sarasti dialogue | ⏳ TODO | Sonnet 3.5 | 200K | 10K | $1 | - | - |
| T010 | Extract Szpindel dialogue | ⏳ TODO | Sonnet 3.5 | 200K | 10K | $1 | - | - |
| T011 | Extract Bates dialogue | ⏳ TODO | Sonnet 3.5 | 200K | 10K | $1 | - | - |
| T012 | Extract Cunningham dialogue | ⏳ TODO | Sonnet 3.5 | 200K | 10K | $1 | - | - |
| T013 | Build jargon dictionary | ⏳ TODO | GPT-4o | 128K | 50K | $5 | - | - |
| T062 | Literary style analysis | ⏳ TODO | Opus 4.1 | 200K | 120K | $20 | - | - |
| T063 | Consolidate character voices | ⏳ TODO | Haiku | 200K | 30K | $1 | - | - |

**Stage 1 Total:** $46 | **Target:** 2-3 weeks | **Longest task:** T062 (120K tokens)

---

### **Stage 2: Summaries (Context Building)**

| ID | Task | Status | LLM | Limit | Req'd | Cost | Started | Done |
|----|------|--------|-----|-------|-------|------|---------|------|
| T014 | Generate chapter summaries (all 22) | ⏳ TODO | Sonnet | 200K | 150K | $10 | - | - |
| T015 | Create character snapshots (all 22) | ⏳ TODO | Sonnet | 200K | 150K | $10 | - | - |
| T016 | Track Chinese Room theme | ⏳ TODO | GPT-4o-mini | 128K | 90K | $1 | - | - |
| T017 | Track consciousness debates | ⏳ TODO | GPT-4o-mini | 128K | 90K | $1 | - | - |

**Stage 2 Total:** $22 | **Target:** 1-2 weeks | **Note:** Can load entire book (Sonnet/200K)

---

### **Stage 3: Translation (Chapter by Chapter)**

> **Context Budget:** Limit: 200K tokens (Opus 4.1) | Req'd: ~55K per chapter | **CRITICAL: Fresh session per chapter**

| ID | Task | Status | LLM | Limit | Req'd | Est. Cost | Owner | Started | Completed |
|----|------|--------|-----|-------|-------|-----------|-------|---------|-----------|
| T018 | Translate Chapter 1 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T019 | Translate Chapter 2 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T020 | Translate Chapter 3 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T021 | Translate Chapter 4 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T022 | Translate Chapter 5 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T023 | Translate Chapter 6 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T024 | Translate Chapter 7 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T025 | Translate Chapter 8 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T026 | Translate Chapter 9 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T027 | Translate Chapter 10 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T028 | Translate Chapter 11 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T029 | Translate Chapter 12 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T030 | Translate Chapter 13 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T031 | Translate Chapter 14 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T032 | Translate Chapter 15 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T033 | Translate Chapter 16 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T034 | Translate Chapter 17 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T035 | Translate Chapter 18 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T036 | Translate Chapter 19 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T037 | Translate Chapter 20 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T038 | Translate Chapter 21 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |
| T039 | Translate Chapter 22 | ⏳ TODO | Opus 4.1 | 200K | 55K | $15 | - | - | - |

**Stage 3 Total:** $330 | **Target:** 3-6 months

---

### **Stage 4: Illustrations (Visual Documentation)**

> **100-ticket range (T200-T299)** for comprehensive illustration pipeline  
> **Context Budget:** Varies by phase - Intelligence (50K), Prompts (5K), Captions (2K)

| ID | Task | Status | LLM | Limit | Req'd | Est. Cost | Owner | Started | Completed |
|----|------|--------|-----|-------|-------|-----------|-------|---------|-----------|
| T200 | Master Orchestrator - Scan all chapters & spawn tickets | ⏳ TODO | Sonnet 3.5 | 200K | 80K | $8 | - | - | - |

**T201-T230: Horror Priority 1 - Alien/Incomprehensible (Est. ~10-12 images)**
| T201 | Scrambler First Contact (3 interpretations) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T202 | Rorschach Structure (organic vs mechanical vs alive) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T203 | Crucifix Glitch Pattern (WARNING) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T204 | The Conversation Scene (incomprehensible communication) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T205 | Sarasti's True Face (predator vs human) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T206 | Scrambler Locomotion (impossible joints) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T207 | Rorschach Interior (multiple sections, all wrong) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T208 | Phase-Shifted Entity (superposition horror) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T209-T212 | [Reserved for T200 spawning] | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |

**T213-T230: Horror Priority 2 - Technical/Disturbing (Est. ~8-10 images)**
| T213 | Vampire Neuroanatomy (predator brain) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T214 | Theseus Non-Euclidean Corridors | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T215 | Interface Pod Violation (body autonomy) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T216 | Gang of Four Switching (personality death) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T217-T230 | [Reserved for T200 spawning] | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |

**T231-T250: Horror Priority 3 - Existential/Isolation (Est. ~6-8 images)**
| T231 | Rorschach First Approach (scale horror) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T232 | Earth from Theseus (abandonment, irrelevance) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T233 | Oort Cloud Emptiness (existential void) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T234 | Theseus Alone (cosmic indifference) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T235-T250 | [Reserved for T200 spawning] | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |

**T251-T260: Horror Priority 4 - Character/Psychological (Est. ~4-6 images)**
| T251 | Szpindel Emotional Overlay (superimposed breakdown) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T252 | Siri's Blindsight Episode (consciousness failure) | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |
| T253-T260 | [Reserved for T200 spawning] | ⏳ TODO | Pipeline | 200K | 57K | $5.35 | - | - | - |

**T261-T299: [Reserved for expansion/additional horror candidates from T200]**

**Stage 4 Target:** 30-35 total illustrations  
**Stage 4 Total Cost:** $168-195 (30-35 images × $5.35 + T200 orchestration)  
**Timeline:** 2-3 weeks (3-4 images per day)  
**Dependencies:** T200 must complete first to spawn specific tickets

**Cost Breakdown per Image:**
- Intelligence Gathering (Sonnet, 50K): $5.00
- Prompt Generation (Haiku, 5K): $0.25
- Caption Refinement (Haiku, 2K): $0.10
- Image Generation (Grok Imagine): $0.00
- **Total:** $5.35 per illustration

**Pipeline Phases (per ticket):**
1. Intelligence Gathering → `Output/Illustrations/Intelligence/T[N]-*.md`
2. Prompt Generation → `Output/Illustrations/Prompts/T[N]-*.md`
3. Image Generation (manual Grok Imagine) → `Output/Illustrations/Final/T[N]-*.png`
4. Caption Refinement → `Output/Illustrations/Captions/T[N]-*.md`

---

### **Stage 5: Reviews (Quality Control)**

> **Context Budget:** Varies by task - reviews need entire manuscript in context (250K-2M tokens depending on LLM)

| ID | Task | Status | LLM | Limit | Req'd | Est. Cost | Owner | Started | Completed |
|----|------|--------|-----|-------|-------|-----------|-------|---------|-----------|
| T040 | Scientific accuracy review | ⏳ TODO | GPT-4o | 128K | 120K | $10 | - | - | - |
| T041 | Internal consistency review | ⏳ TODO | Sonnet 3.5 | 200K | 150K | $8 | - | - | - |
| T042 | Plot integrity review | ⏳ TODO | Gemini 1.5 Pro | 2M | 250K | $5 | - | - | - |
| T043 | Jargon consistency check | ⏳ TODO | GPT-4o-mini | 128K | 80K | $2 | - | - | - |
| T044 | Beta read #1 | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T045 | Beta read #2 | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T046 | Multi-LLM fact-check | ⏳ TODO | Perplexity | - | 150K | $20/mo | - | - | - |
| T047 | Sanity check (backstop) | ⏳ TODO | Grok Fast | 128K | 120K | $0 | - | - | - |
| T048 | Final editorial pass | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T049 | Apply fixes (Opus maintains voice) | ⏳ TODO | Opus 4.1 | 200K | 180K | $20 | - | - | - |

**Stage 5 Total:** $65 | **Target:** 1-2 months

---

### **Stage 6: Publication (Final Outputs)**

> **Context Budget:** Light - most tasks are compilation/tools; T061 preface requires 60K tokens

| ID | Task | Status | LLM | Limit | Req'd | Est. Cost | Owner | Started | Completed |
|----|------|--------|-----|-------|-------|-----------|-------|---------|-----------|
| T049 | Compile manuscript | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T050 | Appendix A: Translation Philosophy | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T051 | Appendix B: From Sarasti | ⏳ TODO | Opus 4.1 | 200K | 40K | $5 | - | - | - |
| T052 | Appendix C: Jargon Guide | ⏳ TODO | Sonnet 3.5 | 200K | 30K | $2 | - | - | - |
| T053 | Appendix D: Reproducibility | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T054 | Generate PDF (Pandoc) | ⏳ TODO | Tool | - | - | $0 | - | - | - |
| T055 | Generate EPUB (Calibre) | ⏳ TODO | Tool | - | - | $0 | - | - | - |
| T056 | Acknowledgments | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T057 | Publish to AO3 | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T058 | Publish to GitHub | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T059 | Marketing blurb | ⏳ TODO | Opus 4.1 | 200K | 20K | $3 | - | - | - |
| T060 | Community outreach | ⏳ TODO | Human | - | - | $0 | - | - | - |
| T061 | Generate Preface | ⏳ TODO | Opus 4.1 | 200K | 60K | $10-15 | - | - | - |

**Stage 6 Total:** $25-30 | **Target:** 2-4 weeks

---

## Overall Project Summary

**Total Tasks:** 140+ (60 base + 80+ illustrations via T200 spawning)  
**Estimated Total Cost:** $620-690  
  - Research: $46
  - Summaries: $22
  - Translation: $330
  - Illustrations: $168-195
  - Reviews: $65
  - Publication: $25-30

**Estimated Timeline:** 7-10 months  

**Phase Completion:**
- [ ] **Stage 1: Research** (0/15 tasks)
- [ ] **Stage 2: Summaries** (0/4 tasks)
- [ ] **Stage 3: Translation** (0/22 tasks)
- [ ] **Stage 4: Illustrations** (0/100+ tasks - T200 spawns specifics)
- [ ] **Stage 5: Reviews** (0/10 tasks)
- [ ] **Stage 6: Publication** (0/13 tasks)
- [ ] **Stage 5: Publication** (0/12 tasks)

---

## Current Blockers

*None - project in planning phase*

---

## Recent Updates

- **2025-01-XX:** Project structure created
- **2025-01-XX:** Documentation complete
- **2025-01-XX:** Kanban board initialized

---

## Next Actions

1. ⏳ Acquire source material (T001)
2. ⏳ Convert to Markdown (T002)
3. ⏳ Begin character studies (T003-T007)

---

**For detailed ticket information, see:** `Instructions/Tickets/TXXX.md`  
**For task outputs, see:** `Tasks/0X-[Stage]/`

---

## LLM Selection Strategy

### **Single Author = Consistent Voice**

**Claude Opus 4.1** is the translator/author for all creative work:
- **All 22 chapter translations** - Superior prose quality, consistent voice throughout
- **Character studies** - Deep understanding and nuanced analysis
- **Appendix B "From Sarasti"** - Requires Opus's voice/personality
- **Fixes during review** - Author maintains own voice when correcting issues
- **Marketing materials** - Premium quality for promotional content

**Why Opus 4.1 as sole author:**
- Demonstrably superior writing quality (see AI Reviews examples)
- Consistent authorial voice across entire book
- Nuanced character understanding and personality
- Worth the premium cost for something people will read for hours
- One "author" prevents stylistic inconsistencies

### **Diverse Reviewers = Catch Different Issues**

Different LLMs for specialized review tasks:

**GPT-4o** - Scientific accuracy and reasoning
- Different training corpus catches what Claude misses
- Strong with technical/scientific validation
- Excellent logical reasoning for consistency checks

**Claude Sonnet 3.5** - Internal consistency analysis
- Same family as Opus, understands authorial intent
- Cost-effective for bulk cross-chapter analysis
- Pattern matching across 22 chapters

**Gemini 1.5 Pro** - Plot integrity
- Massive context window (can hold all chapters simultaneously)
- Different perspective on continuity
- Google's unique training approach

**Perplexity** - Scientific fact-checking
- Web-grounded with current research sources
- Validates neuroscience/physics claims against latest literature
- Catches outdated or incorrect science

**Grok Fast (xAI)** - Sanity check backstop
- Free, unlimited usage
- Final "does this make sense?" pass
- Catches obvious errors other models missed
- No cost = perfect safety net

**GPT-4o-mini** - Jargon consistency checking
- Fast pattern matching for repeated terms
- Cost-effective for mechanical validation
- No creative interpretation (just verification)

### **Critical Principle: Author Applies Own Fixes**

**Opus 4.1 applies all fixes** identified by reviewers:
- Maintains voice consistency
- Prevents "too many cooks" syndrome
- Reviewers identify problems, author solves them
- One authorial vision throughout

### **Cost Breakdown**

| Category | LLM | Tasks | Est. Cost |
|----------|-----|-------|-----------|
| **Author (Translation)** | Opus 4.1 | 22 chapters | $330 |
| **Author (Research)** | Opus 4.1 | 5 character studies | $15 |
| **Author (Fixes)** | Opus 4.1 | Review corrections | $20 |
| **Author (Publication)** | Opus 4.1 | Appendix B, marketing | $8 |
| **Reviews (Multi-LLM)** | GPT-4o, Sonnet, Gemini, etc. | Specialized validation | $45 |
| **Reviews (Free Backstop)** | Grok Fast | Sanity check | $0 |
| **Support** | Sonnet 3.5, GPT-4o, etc. | Summaries, extraction | $34 |
| **Total** | | | **~$452** |

### **Philosophy: Quality Over Economy**

This is a **book people will read**, not a technical document. The $452 investment buys:
- Professional-grade prose quality
- Consistent authorial voice
- Nuanced character understanding
- Multi-perspective quality validation
- Educational value (review process preserved in git history)

**Opus as author + diverse reviewers = best of both worlds: consistency + thoroughness**

---

*"I translate. I process. I track progress without understanding completion."*  
— Project Kanban, v1.1
