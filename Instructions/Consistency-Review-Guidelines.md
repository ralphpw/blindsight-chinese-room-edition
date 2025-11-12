# Internal Consistency Review Guidelines
## Instructions for LLMs

This review ensures consistency across all 22 translated chapters. Run this AFTER all chapters are translated but BEFORE final publication.

---

## Purpose

Catch inconsistencies that emerge from translating chapters separately:
- Character voice variations
- Terminology drift
- Contradictory jargon translations
- Continuity errors introduced by translation
- Tonal shifts between chapters
- **Fair use compliance violations (LEGAL REQUIREMENT)**

---

## Review Categories

### 1. Fair Use Compliance ⚖️ (LEGAL - REVIEW FIRST)

**Check:** No copyright violations that would invalidate fair use claim

**CRITICAL:** This is a legal requirement, not optional. Review this category FIRST before other consistency checks.

**Process:**
1. Read `Instructions/Using-Watts-Language-Legal-Requirements.md` completely
2. Sample 3-5 paragraphs from each chapter
3. Compare against original Watts text
4. Flag any violations

**Legal Violations to Flag:**

**CRITICAL (Must fix immediately):**
- ❌ Verbatim paragraph copying from Watts
- ❌ Extended dialogue (3+ exchanges) transcribed word-for-word
- ❌ Descriptive passages copied without transformation
- ❌ Scene descriptions that are just Watts' text with minor edits

**Acceptable (within fair use):**
- ✅ Sarasti's short commands preserved ("You have thirty seconds.")
- ✅ Technical terminology used exactly ("synthesist," "Chinese Room")
- ✅ Character names and coined words
- ✅ Thematic phrases (recurring motifs)
- ✅ Single sentences for character voice when necessary

**Example Issues:**
```markdown
❌ VIOLATION (paragraph copying):
Chapter 5, paragraph 3:
"[Entire 5-sentence Watts paragraph copied verbatim describing Rorschach]"
FIX: Rewrite description using same concepts, different structure

✅ ACCEPTABLE (phrase-level for character voice):
Sarasti: "You have thirty seconds."
REASON: Character-defining, ultra-minimal, transforming would harm translation

✅ ACCEPTABLE (technical term):
"The synthesist's pattern recognition kicked in..."
REASON: Watts' coined term, necessary for accuracy
```

**Tool:**
```bash
# Spot-check: compare sample paragraphs
# Human review required - LLM should flag suspicious similarities
```

**Output:**
```markdown
### Fair Use Compliance Issues ⚖️
| Chapter | Paragraph/Line | Issue | Violation Type | Legal Risk | Fix |
|---------|----------------|-------|----------------|------------|-----|
| 5 | Para 3 | Verbatim Rorschach description | Paragraph copying | CRITICAL | Rewrite with transformation |
| 12 | Lines 45-67 | Extended Sarasti monologue copied | Extended dialogue | HIGH | Paraphrase keeping voice |
```

---

### 2. Jargon Consistency

**Check:** Same technical term translated identically every time

**Process:**
1. Extract all instances of key technical terms
2. Compare translations across chapters
3. Flag variations

**Example Issues:**
- ❌ Ch 3: "synaptic topology" → "how neurons connect"  
  Ch 7: "synaptic topology" → "brain wiring patterns"
- ✅ Should be consistent: Always "how neurons connect"

**Key Terms to Check:**
- Neuroscience: synaptic, phenomenological, metacognition, consciousness, qualia
- Physics: relativistic, Theseus, Burns-Caulfield, scrambler
- Biology: phenotype, adaptation, vestigial
- Watts neologisms: vampire, Chinese Room, Rorschach

**Tool:**
```bash
# Extract all occurrences of a term
grep -n "synaptic" Tasks/03-Translation/chapters/*.md
```

---

### 3. Character Voice Consistency

**Check:** Each character sounds like themselves across all chapters

**Process:**
1. Extract dialogue per character across all chapters
2. Compare linguistic patterns (word choice, sentence structure, formality)
3. Flag chapters where character voice shifts

**Example Issues:**
- ❌ Sarasti uses contractions in Ch 5 but never elsewhere
- ❌ Keeton suddenly becomes overly technical in Ch 12
- ❌ Szpindel loses humor in Ch 18

**Per Character Checklist:**

**Keeton (POV narrator):**
- [ ] Consistently introspective tone
- [ ] Same level of technical detail throughout
- [ ] Clinical-but-relatable voice maintained
- [ ] First-person narrative voice stable

**Sarasti:**
- [ ] Consistently alien/unsettling
- [ ] Technical precision maintained
- [ ] No warmth/empathy creeping in
- [ ] Command style consistent

**Szpindel:**
- [ ] Humor level consistent
- [ ] Casual language maintained
- [ ] Technical expertise shows through
- [ ] Friendship warmth consistent

**Bates:**
- [ ] Professional military tone
- [ ] Tactical thinking patterns
- [ ] Competence evident
- [ ] Protective nature consistent

**Cunningham:**
- [ ] Multiple personalities tracked separately
- [ ] Each persona consistent with itself
- [ ] Transitions handled similarly
- [ ] Unity/division theme maintained

---

### 4. Recurring Phrases & Motifs

**Check:** Key phrases/concepts worded identically when repeated

**Process:**
1. Identify important recurring concepts
2. Verify same translation used each time
3. Flag variations that break thematic threads

**Key Recurring Elements:**

**"Chinese Room" concept:**
- [ ] Same explanation/analogy used
- [ ] Consistent terminology
- [ ] Philosophical point preserved

**Vampire biology:**
- [ ] Crucifix glitch described consistently
- [ ] Right-angle sensitivity same each time
- [ ] Predator nature maintained

**Consciousness themes:**
- [ ] "Consciousness is a side effect" phrasing
- [ ] Evolutionary arguments consistent
- [ ] Philosophical stance unified

**The Fireflies:**
- [ ] Event described consistently in flashbacks
- [ ] Timeline references align
- [ ] Emotional impact maintained

---

### 5. Scientific Accuracy Consistency

**Check:** Scientific concepts explained same way throughout

**Process:**
1. Extract all scientific explanations
2. Verify consistent level of simplification
3. Flag contradictory simplifications

**Example Issues:**
- ❌ Ch 2: Photons explained in detail  
  Ch 15: Photons assumed known
- ❌ Ch 5: Neurons dumbed down heavily  
  Ch 10: Neuroscience kept technical

**Consistency Rules:**
- First mention = brief explanation
- Subsequent mentions = term only (reader already knows)
- Same complexity level maintained throughout
- No contradictory simplifications

---

### 6. Plot Continuity (Translation-Introduced)

**Check:** Translation didn't introduce plot contradictions

**Process:**
1. Compare original chapter plot points
2. Verify translated versions preserve continuity
3. Flag accidental changes

**Example Issues:**
- ❌ Original: "three days ago"  
  Translation: "last week" (contradiction with timeline)
- ❌ Character name spelled differently between chapters
- ❌ Event sequence altered by translation

**Not Checking:**
- Original plot errors (Watts' responsibility)
- Intentional ambiguities (preserve them)

**Only Flag:**
- Contradictions created by translation process

---

### 7. Tone & Atmosphere Consistency

**Check:** Overall mood maintained across chapters

**Process:**
1. Assess emotional tone per chapter
2. Verify matches original's intended atmosphere
3. Flag jarring tonal shifts

**Target Tone (from original):**
- Clinical but unsettling
- Intellectual horror
- Foreboding throughout
- Cold, analytical, alien

**Example Issues:**
- ❌ Chapter suddenly too warm/friendly
- ❌ Horror atmosphere lost in translation
- ❌ Humor where none existed
- ❌ Sentimentality added

---

### 8. Formatting & Style Consistency

**Check:** Structural elements handled uniformly

**Process:**
1. Review formatting choices (italics, quotes, section breaks)
2. Verify same approach across chapters
3. Standardize variations

**Elements to Check:**

**Ship's log entries:**
- [ ] Formatted identically
- [ ] Timestamps consistent format
- [ ] Technical style maintained

**Flashback sections:**
- [ ] Marked same way (italics/breaks)
- [ ] Tense consistency
- [ ] Transition phrases similar

**Internal monologue:**
- [ ] Distinguished from dialogue consistently
- [ ] Formatting choices maintained

**Chapter openings/closings:**
- [ ] Similar structure
- [ ] Consistent tone setting

---

### 9. Translation Philosophy Adherence

**Check:** All chapters follow same translation principles

**Process:**
1. Review translation approach per chapter
2. Verify adherence to stated philosophy
3. Flag chapters that diverge

**Core Principles (from project docs):**
- [ ] Accessibility maintained (not dumbed down)
- [ ] Scientific accuracy preserved
- [ ] Watts' voice respected
- [ ] Characters distinguishable
- [ ] Atmosphere intact
- [ ] No over-explanation
- [ ] Technical jargon simplified per dictionary

**Red Flags:**
- Chapter that's suddenly harder to read
- Chapter that loses Watts' voice
- Over-simplified chapter (lost nuance)
- Chapter that explains too much

---

## Review Process

### Step 1: Automated Checks (Haiku + Scripts)

```bash
# Extract all jargon terms
grep -i "consciousness\|synaptic\|vampire" chapters/*.md > jargon-check.txt

# Extract all character dialogue
for char in Keeton Sarasti Szpindel Bates; do
  grep "\".*\"" chapters/*.md | grep $char > ${char}-dialogue.txt
done

# Check for common words drift
for term in "scrambler" "Theseus" "fireflies" "vampire"; do
  grep -n "$term" chapters/*.md
done
```

### Step 2: LLM Review (Sonnet)

**Prompt:**
```markdown
TASK: Internal consistency review across all 22 chapters.

CONTEXT: These chapters were translated separately. Check for:
1. Jargon consistency (same term = same translation)
2. Character voice stability
3. Recurring phrase consistency
4. Scientific explanation consistency
5. No translation-introduced plot errors
6. Tone/atmosphere maintained
7. Formatting standardized
8. Translation philosophy adherence

INPUTS: All 22 translated chapters + jargon dictionary

OUTPUTS: 
- List of inconsistencies found
- Specific chapter/line references
- Suggested fixes
- Severity rating (critical/moderate/minor)

FORMAT: Markdown table with columns:
| Issue | Chapters | Severity | Suggested Fix |
```

### Step 3: Human Review

- Review LLM findings
- Prioritize critical issues
- Make editorial decisions on edge cases
- Apply fixes systematically

### Step 4: Re-check

- Run automated checks again
- Verify fixes didn't introduce new issues
- Spot-check random sections

---

## Output Format

```markdown
# Internal Consistency Review Report

## Executive Summary
- Total issues found: [X]
- Critical: [X]
- Moderate: [X]
- Minor: [X]

## Jargon Consistency Issues

| Term | Chapters | Variations | Recommended |
|------|----------|------------|-------------|
| synaptic | 3, 7, 12 | "brain wiring", "neural connections", "how neurons connect" | "how neurons connect" (per dictionary) |

## Character Voice Issues

| Character | Chapters | Issue | Fix |
|-----------|----------|-------|-----|
| Sarasti | 5 | Uses contraction "don't" | Change to "do not" |

## [Additional Categories...]

## Priority Fixes

1. [Critical issue with specific fix]
2. [Critical issue with specific fix]
...

## Sign-off

- [ ] All critical issues resolved
- [ ] Moderate issues reviewed (human decision)
- [ ] Minor issues documented (fix if easy)
- [ ] Re-check passed
- [ ] Ready for final review phase
```

---

## Quality Gates

Before marking this review complete:

- [ ] All automated checks run successfully
- [ ] LLM review completed for all chapters
- [ ] Human reviewed all critical findings
- [ ] Fixes applied and verified
- [ ] No new inconsistencies introduced
- [ ] Report generated and archived
- [ ] Sign-off from human reviewer

---

## When to Run This Review

**Timing:** After T039 (final chapter translation), before T040 (scientific accuracy review)

**Dependencies:**
- All 22 chapters translated
- Jargon dictionary finalized
- Character studies available for reference

**Estimated Time:** 4-6 hours (automated + LLM + human review)

**Estimated Cost:** $8 (Sonnet for cross-chapter analysis)

---

## Success Criteria

This review ensures:
1. **Reader Experience**: No jarring inconsistencies breaking immersion
2. **Professional Quality**: Book reads as unified whole, not 22 separate pieces
3. **Translation Integrity**: Philosophy applied consistently
4. **Character Authenticity**: Each voice stable throughout
5. **Technical Coherence**: Science explained at consistent level

**A translation can be individually excellent per chapter but fail as a whole if inconsistent. This review prevents that.**

---

*This file is referenced by T041 and any consistency-related tasks.*
