# Ticket Generation Guide

This guide helps you quickly create the remaining 54 ticket files using the template.

---

## Quick Reference: All 60 Tickets

### **Stage 1: Research (T001-T013)** - $25-30, 2-3 weeks
- ✅ T001: Acquire Source Material (Human, $0)
- ✅ T002: Convert to Markdown (Human/Script, $0)
- ✅ T003: Keeton Character Study (Opus, $3)
- 🔲 T004: Sarasti Character Study (Opus, $3)
- 🔲 T005: Szpindel Character Study (Opus, $2)
- 🔲 T006: Bates Character Study (Opus, $2)
- 🔲 T007: Cunningham Character Study (Opus, $2)
- 🔲 T008: Extract Keeton Dialogue (Haiku, $1)
- 🔲 T009: Extract Sarasti Dialogue (Haiku, $1)
- 🔲 T010: Extract Szpindel Dialogue (Haiku, $1)
- 🔲 T011: Extract Bates Dialogue (Haiku, $1)
- 🔲 T012: Extract Cunningham Dialogue (Haiku, $1)
- ✅ T013: Build Jargon Dictionary (GPT-4o, $5)

### **Stage 2: Summaries (T014-T017)** - $22, 1-2 weeks
- 🔲 T014: Chapter Summaries 1-11 (Sonnet, $8)
- 🔲 T015: Chapter Summaries 12-22 (Sonnet, $8)
- 🔲 T016: Character Snapshots 1-11 (GPT-4o-mini, $3)
- 🔲 T017: Character Snapshots 12-22 (GPT-4o-mini, $3)

### **Stage 3: Translation (T018-T039)** - $76, 3-6 months
**Opus Chapters (critical/complex):**
- ✅ T018: Chapter 1 (Opus, $10) - FOUNDATION
- 🔲 T021: Chapter 4 (Opus, $7) - First Sarasti deep dive
- 🔲 T029: Chapter 12 (Opus, $8) - Turning point
- 🔲 T037: Chapter 20 (Opus, $10) - Climax

**Sonnet Chapters (standard quality):**
- 🔲 T019: Chapter 2 (Sonnet, $2)
- 🔲 T020: Chapter 3 (Sonnet, $2)
- 🔲 T022: Chapter 5 (Sonnet, $2)
- 🔲 T023: Chapter 6 (Sonnet, $2)
- 🔲 T024: Chapter 7 (Sonnet, $2)
- 🔲 T025: Chapter 8 (Sonnet, $2)
- 🔲 T026: Chapter 9 (Sonnet, $2)
- 🔲 T027: Chapter 10 (Sonnet, $2)
- 🔲 T028: Chapter 11 (Sonnet, $2)
- 🔲 T030: Chapter 13 (Sonnet, $2)
- 🔲 T031: Chapter 14 (Sonnet, $2)
- 🔲 T032: Chapter 15 (Sonnet, $2)
- 🔲 T033: Chapter 16 (Sonnet, $2)
- 🔲 T034: Chapter 17 (Sonnet, $2)
- 🔲 T035: Chapter 18 (Sonnet, $2)
- 🔲 T036: Chapter 19 (Sonnet, $2)
- 🔲 T038: Chapter 21 (Sonnet, $2)
- 🔲 T039: Chapter 22 (Sonnet, $2)

### **Stage 4: Reviews (T040-T047)** - $48, 1-2 months
- 🔲 T040: Scientific Accuracy Review (GPT-4o, $10)
- 🔲 T041: Character Consistency Review (Sonnet, $6)
- 🔲 T042: Plot Integrity Review (Gemini, $4)
- 🔲 T043: Jargon Consistency Review (GPT-4o-mini, $2)
- 🔲 T044: Blind Beta Read #1 (Human, $0)
- 🔲 T045: Blind Beta Read #2 (Human, $0)
- 🔲 T046: Multi-LLM Fact-Check (Perplexity, $6)
- 🔲 T047: Final Human Editorial Pass (Human, $0)

### **Stage 5: Publication (T048-T060)** - $5, 2-4 weeks
- 🔲 T048: Compile Full Manuscript (Haiku, $1)
- 🔲 T049: Create Appendix A (Translation Philosophy) (Human, $0)
- 🔲 T050: Create Appendix B (From Sarasti) (Sonnet, $2)
- 🔲 T051: Create Appendix C (Jargon Guide) (Haiku, $0.50)
- 🔲 T052: Create Acknowledgments (Human, $0)
- 🔲 T053: Generate PDF (Pandoc, $0)
- 🔲 T054: Generate EPUB (Calibre, $0)
- 🔲 T055: Upload to AO3 (Human, $0)
- 🔲 T056: Upload to GitHub (Human, $0)
- 🔲 T057: Create Marketing Blurb (Sonnet, $1)
- 🔲 T058: Announce on r/printSF (Human, $0)
- 🔲 T059: Notify Peter Watts (Human, $0)
- 🔲 T060: Final Archive (Human, $0)

---

## Generation Instructions

### For Character Studies (T004-T007):
**Pattern:** Copy T003, change character name
- Same LLM (Opus)
- Same cost ($2-3)
- Same structure (Background, Communication, Translation Rules)
- Adjust expected output to character complexity

### For Dialogue Extraction (T008-T012):
**Pattern:** Simple extraction task
- LLM: Haiku
- Cost: $1 each
- Process: grep all dialogue by character, create bank
- Output: `[character]-all-dialogue.md`

### For Chapter Summaries (T014-T015):
**Pattern:** Batch chapters
- LLM: Sonnet
- Cost: $8 each batch
- 11 chapters per task
- Output: Plot beats, character changes, key jargon

### For Character Snapshots (T016-T017):
**Pattern:** Emotional/mental states per chapter
- LLM: GPT-4o-mini
- Cost: $3 each batch
- Output: Method-acting reference (emotional state at chapter start)

### For Sonnet Chapter Translations (T019-T039, excluding Opus chapters):
**Pattern:** Copy T018, swap to Sonnet
- Cost: $2 per chapter
- Same context requirements
- Same quality gates
- Note: Only use after T018 establishes voice

### For Reviews (T040-T047):
**Pattern:** Specific review lens per task
- T040: Scientific accuracy (neuroscience, physics)
- T041: Voice consistency (Keeton sounds like Keeton)
- T042: Plot integrity (nothing missing)
- T043: Jargon consistency (same term = same translation)
- T044-T045: Blind human reads (fresh eyes)
- T046: Multi-LLM fact-check (Perplexity for citations)
- T047: Final editorial (human polish)

### For Publication (T048-T060):
**Pattern:** Final outputs
- Mostly human/tool tasks ($0)
- Some Haiku/Sonnet for automation ($1-2)
- Pandoc/Calibre for format conversion

---

## Creation Strategy

You can create tickets:

1. **All at once:** Generate all 54 remaining files
2. **By stage:** Generate stage 1 tickets now, stage 2 when ready
3. **Just-in-time:** Create tickets as you reach them in workflow
4. **Batch by type:** All character studies, then all extractions, etc.

**Recommendation:** Create **Stage 1 tickets now** (T004-T012 = 9 files) since that's the immediate work. Generate later stages as you progress.

---

## Automation Tip

For Cursor/Copilot agents, you can:
1. Point agent to TEMPLATE.md
2. Give it this reference guide
3. Say: "Generate T004 through T012 using the template"
4. Agent will batch-create all 9 files

---

## Dependencies

**Critical Path:**
- T001-T002 must complete first (source material)
- T003-T007 can run in parallel (character studies)
- T008-T012 depend on T002 (dialogue extraction needs Markdown)
- T013 depends on T002 (jargon needs Markdown)
- T014-T017 depend on all of Stage 1
- T018 depends on all of Stages 1 & 2
- T019-T039 depend on T018 (voice established)
- T040-T047 depend on all translations complete
- T048-T060 depend on reviews complete

---

**Total Tickets:** 60  
**Created:** 6 (T001-T003, T013, T018, TEMPLATE)  
**Remaining:** 54
