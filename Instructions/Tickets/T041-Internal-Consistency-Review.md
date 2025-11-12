# T041: Internal Consistency Review

**Stage:** 4-Reviews  
**Status:** TODO  
**LLM:** Sonnet + Scripts  
**Estimated Cost:** $8  
**Estimated Time:** 4-6 hours  
**Depends On:** T039 (all chapters translated)

---

## Context Requirements

**Documents to Read BEFORE Starting:**

- [ ] `Instructions/Consistency-Review-Guidelines.md` - Complete review framework and criteria
- [ ] `Instructions/Using-Watts-Language-Legal-Requirements.md` - **LEGAL:** Fair use compliance requirements
- [ ] `Documentation/The-Preface.md` - Voice baseline for consistency checking
- [ ] `Documentation/Character-Philosophy.md` - Character voice requirements
- [ ] `Tasks/01-Research/Jargon-Dictionary.md` (T013 output) - Terminology reference
- [ ] All 22 translated chapters (T018-T040 outputs)

**Critical:** Must have the review guidelines and baseline voice fresh to catch subtle inconsistencies. Must verify fair use compliance.

---

## Objective

Ensure consistency across all 22 translated chapters: jargon usage, character voices, recurring phrases, tone, and formatting.

---

## Why This Matters

**Problem:** Chapters translated separately may have:
- Same term translated differently (jargon drift)
- Character voice variations between chapters
- Inconsistent explanations of recurring concepts
- Tonal shifts that break atmosphere
- Formatting inconsistencies

**Solution:** Systematic cross-chapter consistency review.

---

## Process

### 1. Load Consistency Guidelines

**Required Reading:**
- `Instructions/Consistency-Review-Guidelines.md` (complete reference)
- `Tasks/01-Research/jargon-analysis/jargon-dictionary.md`
- Character studies (T003-T007 outputs)

### 2. Run Automated Checks

**Scripts to execute:**

```powershell
# Navigate to chapters folder
cd "Tasks/03-Translation/chapters"

# Extract jargon usage
Select-String -Pattern "consciousness|synaptic|vampire|scrambler|Theseus" -Path *.md `
  | Out-File "../../consistency-checks/jargon-occurrences.txt"

# Extract character dialogue
foreach ($char in @("Keeton", "Sarasti", "Szpindel", "Bates", "Cunningham")) {
  Select-String -Pattern "`".*`"" -Path *.md `
    | Select-String $char `
    | Out-File "../../consistency-checks/$char-dialogue.txt"
}

# Check recurring phrases
foreach ($phrase in @("Chinese Room", "right-angle", "Fireflies")) {
  Select-String -Pattern $phrase -Path *.md -Context 1 `
    | Out-File "../../consistency-checks/phrase-$phrase.txt"
}
```

### 3. LLM Consistency Analysis (Sonnet)

**Context Required:**
- All 22 translated chapters
- Jargon dictionary
- Character voice profiles
- Consistency guidelines

**Prompt:**
```markdown
TASK: Cross-chapter internal consistency review

LOAD CONTEXT:
- All 22 chapters (Tasks/03-Translation/chapters/)
- Jargon dictionary (Tasks/01-Research/jargon-analysis/jargon-dictionary.md)
- Consistency guidelines (Instructions/Consistency-Review-Guidelines.md)

REVIEW FOR:

1. **Jargon Consistency**
   - Same technical term always translated identically
   - Check: consciousness, synaptic, vampire, scrambler, Theseus, etc.
   - Flag: Any variation in translation of same term

2. **Character Voice Consistency**
   - Keeton: Clinical, introspective, relatable throughout
   - Sarasti: Alien, unsettling, no warmth ever
   - Szpindel: Humorous, casual, competent throughout
   - Bates: Military professional, protective throughout
   - Cunningham: Each persona consistent with itself
   - Flag: Any chapter where character sounds different

3. **Recurring Phrases**
   - "Chinese Room" explained consistently
   - Vampire biology described same way
   - Consciousness themes unified
   - Fireflies event consistent in flashbacks

4. **Scientific Explanations**
   - Same concept explained at same complexity level
   - No contradictory simplifications
   - Consistent depth throughout

5. **Tone & Atmosphere**
   - Clinical, unsettling, intellectual horror maintained
   - No jarring warmth/sentimentality
   - Foreboding preserved

6. **Formatting**
   - Ship's log entries uniform
   - Flashbacks marked consistently
   - Internal monologue handled same way

7. **Fair Use Compliance** ⚖️
   - No verbatim paragraphs copied from Watts (legal violation)
   - Sarasti's short commands preserved correctly (phrase-level OK)
   - Descriptive passages transformed (not copied)
   - Technical terms used appropriately (common language OK)
   - Extended dialogue paraphrased (not transcribed)
   - Flag: Any paragraph-level copying that violates fair use

OUTPUT FORMAT:

# Internal Consistency Review Report

## Executive Summary
- Total issues: [count]
- Critical: [count]
- Moderate: [count]  
- Minor: [count]

## Issues by Category

### Jargon Inconsistencies
| Term | Chapters | Variations Found | Dictionary Standard | Fix Required |
|------|----------|------------------|---------------------|--------------|
| [term] | [#s] | [list] | [correct] | [Yes/No] |

### Character Voice Issues
| Character | Chapters | Issue Description | Severity | Suggested Fix |
|-----------|----------|-------------------|----------|---------------|
| [name] | [#s] | [description] | [C/M/m] | [fix] |

### Recurring Phrase Issues
[Similar table format]

### Scientific Explanation Issues
[Similar table format]

### Tone Issues
[Similar table format]

### Formatting Issues
[Similar table format]

### Fair Use Compliance Issues ⚖️
| Chapter | Issue | Type | Violation | Fix Required |
|---------|-------|------|-----------|--------------|
| [#] | [description] | [Paragraph copy / Extended dialogue / etc.] | [Legal risk level] | [How to transform] |

**Legal Risk Levels:**
- **CRITICAL:** Verbatim paragraph copying (must fix immediately)
- **HIGH:** Extended dialogue transcription (must paraphrase)
- **MEDIUM:** Overuse of exact phrases (review and vary)
- **LOW:** Technical terms (likely OK, verify)

## Priority Fixes (Critical Only)
1. [Issue with chapter/line reference and specific fix]
2. [Issue with chapter/line reference and specific fix]
...

## Recommendations
- [Overall observations]
- [Patterns noticed]
- [Systematic fixes needed]

## Sign-off Checklist
- [ ] All categories reviewed (including fair use compliance)
- [ ] Critical issues flagged
- [ ] Specific line references provided
- [ ] Fixes are actionable
- [ ] No legal violations remain (fair use compliant)
```

### 4. Human Review

**Human reviews LLM report and:**
1. Validates critical issues (are they real problems?)
2. Makes editorial decisions on moderate issues
3. Prioritizes fixes
4. Applies fixes systematically

### 5. Apply Fixes

**For each critical issue:**
1. Locate in source chapter file
2. Apply recommended fix
3. Verify against jargon dictionary / character studies
4. Update change log

### 6. Re-check

**After fixes applied:**
```powershell
# Re-run automated checks
# Compare to baseline
# Verify no new issues introduced
```

### 7. Final Validation

- [ ] All critical issues resolved
- [ ] Spot-check 10 random cross-chapter references
- [ ] Character dialogue samples checked
- [ ] Jargon usage verified in 5 chapters
- [ ] Sign-off report complete

---

## Inputs Required

- [ ] All 22 translated chapters (T018-T039 outputs)
- [ ] Jargon dictionary (T013 output)
- [ ] Character studies (T003-T007 outputs)
- [ ] Consistency guidelines file

---

## Outputs

```
Tasks/04-Reviews/consistency/
├── consistency-report.md (full LLM report)
├── critical-fixes-applied.md (change log)
├── automated-checks/ (script outputs)
│   ├── jargon-occurrences.txt
│   ├── Keeton-dialogue.txt
│   ├── Sarasti-dialogue.txt
│   ├── [etc.]
└── sign-off.md (human validation)
```

---

## Quality Gates

- [ ] Automated checks completed
- [ ] LLM analysis run on all 22 chapters
- [ ] Report generated with specific line references
- [ ] All critical issues addressed
- [ ] Human reviewed and signed off
- [ ] Re-check passed
- [ ] No new inconsistencies introduced

---

## LLM Configuration

**Model:** Claude Sonnet 3.5  
**Why:** Needs to analyze 22 chapters cross-comparison, Sonnet can handle large context  
**Context Window:** ~150K tokens (all chapters + guidelines)  
**Temperature:** 0.2 (precise analysis, not creative)  
**Max Output:** ~20K tokens (comprehensive report)

**Cost Breakdown:**
- Input: ~150K tokens × $3/1M = $0.45
- Output: ~20K tokens × $15/1M = $0.30
- Multiple iterations: ~$8 total

---

## Success Criteria

This review ensures:
1. **No jargon drift** - Same term = same translation always
2. **Character voices stable** - Each character sounds like themselves throughout
3. **Thematic consistency** - Recurring concepts explained uniformly
4. **Professional polish** - Reads as unified whole, not 22 pieces
5. **Translation integrity** - Philosophy applied consistently

**The book must feel like ONE translation, not 22 separate ones.**

---

## Notes

- This is separate from T040 (scientific accuracy) and T042 (plot integrity)
- Focuses specifically on consistency between chapters
- Prevents "seams" showing between separately-translated sections
- Critical for reader immersion and professional quality

**Think of this as "stitching" the 22 chapters into a seamless whole.**

---

**Previous Task:** T040 (Scientific Accuracy Review)  
**Next Task:** T042 (Plot Integrity Review)
