# T047: Sanity Check Review (Grok Fast Backstop)

**Stage:** 4-Reviews  
**Status:** TODO  
**LLM:** Grok Fast (xAI)  
**Estimated Cost:** $0 (free, unlimited)  
**Estimated Time:** 2-3 hours  
**Depends On:** T040-T046 (all other reviews complete)

---

## Context Requirements

**Documents to Read BEFORE Starting:**

- [ ] `Documentation/The-Preface.md` - Voice and tone baseline
- [ ] `Documentation/Audience-Analysis.md` - Target reader profile (bounced readers)
- [ ] Sample chapters (Ch 1, 5, 10, 15, 20) - Representative spread
- [ ] `Tasks/04-Reviews/Review-Summary.md` (if available) - Known issues from other reviews

**Critical:** Fresh perspective matters - don't over-contextualize. Grok should read like a smart first-time reader.

---

## Objective

Final "sanity check" pass using free Grok Fast to catch obvious errors that slipped through other reviews. Acts as a backstop before human editorial pass.

---

## Why Grok Fast?

**Free Safety Net:**
- Unlimited usage, no cost
- Different training approach than Claude/GPT/Gemini
- Fresh perspective after multiple reviews
- Perfect for "does this make sense?" validation

**Role as Backstop:**
- NOT primary reviewer (other LLMs handle that)
- Catches glaring errors others missed
- Quick sanity check before expensive human review
- No cost = can be generous with re-runs

---

## Process

### 1. Load Context

**Required:**
- All 22 translated chapters
- Previous review reports (T040-T046)
- List of issues already identified and fixed

### 2. Run Sanity Check

**Grok Fast Prompt:**
```markdown
TASK: Final sanity check of translated novel

You are the last automated reviewer before human editorial pass. Other LLMs have already done:
- Scientific accuracy review (GPT-4o)
- Internal consistency review (Sonnet)
- Plot integrity review (Gemini)
- Jargon consistency (GPT-4o-mini)
- Fact-checking (Perplexity)

YOUR JOB: Catch obvious errors they missed.

READ: All 22 chapters

LOOK FOR:
1. **Obvious plot holes** - things that make no sense
2. **Character names wrong** - misattributed dialogue, name typos
3. **Timeline contradictions** - "yesterday" vs "last week" mismatches
4. **Tone breaks** - sudden shifts from clinical to casual
5. **Incomplete sentences** - fragments or cut-off text
6. **Repetition** - same phrase used twice in paragraph
7. **Translation artifacts** - "as an AI" type leakage
8. **Formatting issues** - broken italics, missing quotes
9. **Common sense violations** - physics/logic impossibilities
10. **Anything that makes you go "wait, what?"**

OUTPUT FORMAT:

# Grok Fast Sanity Check Report

## Critical Issues (Fix Immediately)
| Chapter | Issue | Type | Quote |
|---------|-------|------|-------|
| Ch 7 | Character name typo | Name | "Sazpindel" should be "Szpindel" |

## Moderate Issues (Review)
[Same format]

## Minor Issues (Optional)
[Same format]

## Overall Assessment
- Does the book make sense as a whole? YES/NO
- Are there any show-stopping issues? YES/NO
- Ready for human editorial pass? YES/NO

## Notes
[Anything else worth mentioning]
```

### 3. Review Grok Output

**Human reviews report for:**
- False positives (Grok flagged non-issues)
- True issues missed by other reviews
- Prioritization (critical vs nice-to-have)

### 4. Apply Critical Fixes

**Only fix critical issues:**
- Plot holes
- Character name errors
- Timeline contradictions
- Incomplete text

**Defer to human:**
- Stylistic preferences
- Judgment calls
- Minor polish

### 5. Re-run if Needed

**Because Grok is free:**
- Can re-run after fixes
- Verify critical issues resolved
- No cost concern for multiple passes

---

## Inputs Required

- [ ] All 22 translated chapters
- [ ] Previous review reports (T040-T046)
- [ ] List of known issues already fixed

---

## Outputs

```
Tasks/04-Reviews/grok-sanity-check/
├── sanity-check-report.md (full Grok output)
├── critical-issues.md (human triage)
├── fixes-applied.md (change log)
└── final-validation.md (Grok re-run confirmation)
```

---

## Quality Gates

- [ ] Grok Fast review completed
- [ ] Report generated with specific chapter/line references
- [ ] Critical issues triaged by human
- [ ] Show-stopping issues fixed (if any)
- [ ] Re-run confirms fixes worked
- [ ] "Ready for human editorial" = YES

---

## LLM Configuration

**Model:** Grok Fast (xAI)  
**Why:** Free, unlimited, different perspective, good at common sense checks  
**Context:** All 22 chapters + previous review summaries  
**Temperature:** 0.3 (mostly factual, some interpretation)  
**Cost:** $0 (free)

---

## Success Criteria

This backstop ensures:
1. **Catch the Obvious:** Things humans will immediately notice
2. **Free Safety Net:** No cost to be thorough
3. **Fresh Eyes:** Different training = different blind spots
4. **Confidence:** Human reviewer can focus on polish, not hunting bugs

**If Grok finds major issues, something went wrong in earlier reviews. If Grok finds nothing critical, proceed with confidence.**

---

## What This Is NOT

❌ Not primary review (that's T040-T046)  
❌ Not stylistic polish (that's human T048)  
❌ Not quality bar (Opus set that)  
❌ Not expensive (it's free!)

✅ Safety net  
✅ Sanity check  
✅ Confidence builder  
✅ "Did we miss anything obvious?"

---

## Notes

- Grok's irreverent personality might flag things as "issues" that are intentional (Watts' style)
- Human triage essential - don't auto-apply Grok fixes
- Because it's free, be generous with re-runs
- Perfect final check before expensive human editorial time

**Free = we can afford to be paranoid. Use it.**

---

**Previous Task:** T046 (Multi-LLM fact-check)  
**Next Task:** T048 (Final human editorial pass)
