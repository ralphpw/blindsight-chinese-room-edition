# T018: Translate Chapter 1 (CRITICAL)

**Stage:** 3-Translation  
**Status:** TODO  
**LLM:** Claude Opus 3.5  
**Estimated Cost:** $10  
**Estimated Time:** 4-6 hours  
**Depends On:** T003-T012 (Character studies), T013 (Jargon), T014-T017 (Summaries)

---

## Context Requirements

**Documents to Read BEFORE Starting:**

**MANDATORY (Must be fresh in memory):**
- [ ] `Documentation/The-Preface.md` - **CRITICAL:** Keep Sarasti-9947 voice and meta-ironic tone fresh
- [ ] `Tasks/01-Research/Literary-Style-Guide.md` (T062 output) - **CRITICAL:** Watts' prose techniques and patterns
- [ ] `Instructions/Character-Voice-Reference.md` - **CRITICAL:** All character voices (human AND non-human) in one document
- [ ] `Instructions/Using-Watts-Language-Legal-Requirements.md` - **LEGAL:** When to use Watts' exact words vs. transform (fair use compliance)
- [ ] `Documentation/Character-Philosophy.md` - Voice profiles and method acting approach

**Supporting Context:**
- [ ] `Tasks/01-Research/Jargon-Dictionary.md` (T013 output) - Technical terms reference
- [ ] `Tasks/02-Summaries/Chapter-01-Summary.md` (T014 output) - Chapter overview
- [ ] `Tasks/02-Summaries/Character-Arc-Snapshot-Chapter-01.md` (T015 output) - Character states
- [ ] Original `Source/Chapter-01.md` (T002 output) - Source material

**Critical:** The preface establishes our voice. Re-read it immediately before translation to ensure consistency.

---

## Objective

---

## Objective

Translate Chapter 1 of *Blindsight* using premium Opus model. This chapter establishes voice for the entire project and must be exceptional quality.

---

## Why Opus for Chapter 1

**Critical Importance:**
- First chapter sets tone for all 22 chapters
- Establishes Keeton's narrative voice (POV for entire book)
- Introduces major characters (first impressions matter)
- Reader's entry point (if this fails, they bounce)

**Opus Advantages:**
- Best prose quality ($10 vs. $2 is worth it)
- Deepest character understanding
- Most nuanced voice differentiation

---

## Process

### 1. Load Context

**Required Files:**
- `Tasks/01-Research/source-material/chapter-01-original.md`
- `Tasks/02-Summaries/character-snapshots/chapter-01-states.md`
- `Tasks/02-Summaries/chapter-summaries/chapter-01-summary.md`
- `Tasks/01-Research/jargon-analysis/jargon-dictionary.md`
- `Tasks/01-Research/dialogue-extraction/keeton-all-dialogue.md`
- `Tasks/01-Research/dialogue-extraction/sarasti-all-dialogue.md`
- `Tasks/03-Translation/prompts/system-prompt-base.md`
- `Tasks/03-Translation/prompts/character-voice-*.md` (all 5)

### 2. Execute Translation

**LLM Prompt Structure:**
```markdown
SYSTEM: [Load system-prompt-base.md]

CONTEXT: You are translating Chapter 1 of Blindsight.

CHARACTER STATES (this chapter):
[Load chapter-01-states.md]

JARGON RULES:
[Load jargon-dictionary.md - key terms only]

TASK: Translate the following chapter using character voice profiles.

[Paste chapter-01-original.md]

OUTPUT: Translated chapter only (no meta-commentary)
```

### 3. Human Review

**Check:**
- [ ] Plot beats preserved (Fireflies event, recruitment)
- [ ] Keeton's voice relatable (not too technical)
- [ ] Sarasti unsettling (technical but comprehensible)
- [ ] Scientific accuracy (neuroscience concepts correct)
- [ ] Atmosphere intact (foreboding, clinical)
- [ ] Word count 80-120% of original

### 4. Update Character Snapshots

After translation, update `Tasks/02-Summaries/character-snapshots/chapter-02-states.md` based on:
- How characters changed in this chapter
- What just happened affecting mental states
- Voice adjustments for next chapter

---

## Outputs

```
Tasks/03-Translation/chapters/chapter-01-translated.md
Tasks/03-Translation/change-logs/chapter-01-changes.md
Tasks/02-Summaries/character-snapshots/chapter-02-states.md (updated)
```

---

## Quality Gates

- [ ] All plot beats from original present
- [ ] Keeton's voice distinct from Sarasti's
- [ ] Technical jargon translated per dictionary
- [ ] Atmosphere preserved (unsettling)
- [ ] No scientific inaccuracies introduced
- [ ] Chapter 2 character snapshots updated
- [ ] Human validation complete

---

## LLM Configuration

**Model:** Claude Opus 3.5  
**Why:** Best quality for foundational chapter  
**Context Window:** ~40K tokens (chapter + all context)  
**Temperature:** 0.7 (creative but controlled)  
**Max Output:** ~30K tokens (translated chapter)

**Cost Breakdown:**
- Input: ~40K tokens × $15/1M = $0.60
- Output: ~30K tokens × $75/1M = $2.25
- **Total: ~$3** (estimate $10 to be safe with iterations)

---

## Success Criteria

**This chapter must:**
1. Be readable without neuroscience PhD
2. Make readers want to read Chapter 2
3. Establish Keeton as relatable POV
4. Preserve Watts' unsettling atmosphere
5. Set voice standards for remaining 21 chapters

**If this fails, the entire project fails.**

---

## Notes

- **DO NOT RUSH THIS**
- Worth spending extra time on human review
- Consider having 2-3 beta readers check this chapter before proceeding
- If voice feels wrong, iterate (Opus cost is worth getting this right)
- This is the proof-of-concept for entire translation approach

---

## Comparison Test

After translation, create side-by-side comparison:
- Original paragraph
- Translated paragraph
- Does translated preserve meaning + improve readability?

If not clearly better, revise approach.

---

**Previous Tasks:** All Stage 1 & 2 tasks  
**Next Task:** T019 (Chapter 2 - can use Sonnet after Ch1 establishes voice)
