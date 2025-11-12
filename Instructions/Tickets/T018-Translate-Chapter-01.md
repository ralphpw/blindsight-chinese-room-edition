# T018: Translate Chapter 1 (CRITICAL)

**Stage:** 3-Translation  
**Status:** TODO  
**LLM:** Claude Opus 3.5  
**Estimated Cost:** $10  
**Estimated Time:** 4-6 hours  
**Depends On:** T002, T003-T007, T008-T012, T013, T014, T015

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
