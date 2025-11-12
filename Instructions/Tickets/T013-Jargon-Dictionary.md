# T013: Build Jargon Dictionary

**Stage:** 1-Research  
**Status:** TODO  
**LLM:** GPT-4o  
**Estimated Cost:** $5  
**Estimated Time:** 3-4 hours  
**Depends On:** T002

---

## Objective

Create comprehensive technical-to-accessible term mapping for all jargon in *Blindsight* (neuroscience, physics, Watts neologisms).

---

## Process

### 1. Extract All Technical Terms

Use GPT-4o (strong with technical vocabulary) to scan all 22 chapters and identify:
- Neuroscience terms (e.g., "synaptic topology," "metacognition")
- Physics/space terms (e.g., "relativistic effects," "Theseus")
- Biology terms (e.g., "phenotype," "adaptation")
- Watts' invented terms (e.g., "scrambler," "Chinese Room")

### 2. Create Translation Mappings

For each term, provide:
- **Original:** Technical jargon as Watts wrote it
- **Simple:** Accessible translation
- **Context:** When to use (formal vs. dialogue)
- **Example:** Before/after in sentence

### 3. Categorize

Organize into sections:
- Neuroscience (100+ terms)
- Physics/Space (50+ terms)
- Biology (30+ terms)
- Watts Neologisms (20+ terms)
- General Technical (misc)

### 4. Human Validation

- Verify scientific accuracy of simplified terms
- Ensure translations don't lose meaning
- Check consistency across categories

---

## LLM Prompt

```markdown
You are creating a jargon dictionary for Peter Watts' Blindsight.

TASK: Extract every technical term from all 22 chapters and create accessible translations.

FORMAT for each entry:

### [TERM]
- **Original Usage:** "The synaptic topology suggested metacognitive recursion."
- **Simplified:** "How neurons connect" or "thinking about thinking"
- **Translation Rule:** In dialogue/narration, use simpler form unless character is Sarasti
- **Example Transformation:**
  - BEFORE: "Phenomenological barriers prevented epistemic closure."
  - AFTER: "We couldn't understand them, no matter how hard we tried."

CATEGORIES:
1. Neuroscience (brain, neurons, consciousness terms)
2. Physics (space, relativity, technology)
3. Biology (evolution, adaptation, xenobiology)
4. Watts Neologisms (scrambler, Theseus, etc.)
5. General Technical

TARGET: 200+ terms minimum

OUTPUT: Markdown with clear categorization and examples
```

---

## Outputs

```
Tasks/01-Research/jargon-analysis/
├── jargon-dictionary.md (comprehensive, 200+ terms)
├── neuroscience-terms.md (subset for reference)
├── physics-terms.md (subset for reference)
└── watts-neologisms.md (subset for reference)
```

---

## Quality Gates

- [ ] 200+ terms mapped
- [ ] All categories populated
- [ ] Each term has: original, simple, example
- [ ] Scientific accuracy validated
- [ ] No meaning lost in simplification
- [ ] Consistency rules clear

---

## LLM Configuration

**Model:** GPT-4o  
**Why:** Strong with technical terminology, good at pattern recognition  
**Context:** All 22 chapters  
**Temperature:** 0.2 (precise, factual)

---

## Success Criteria

This dictionary will be used by every chapter translation to ensure:
- **Consistency:** Same term always translated same way
- **Accuracy:** No scientific errors introduced
- **Accessibility:** Readers without PhDs can understand

---

## Notes

- This is CRITICAL for translation quality
- Inconsistency here = inconsistency in final product
- Worth spending extra time to get right
- Some Watts neologisms should stay (e.g., "scrambler" is the name)
- Others need context clues added (explain on first use)

---

**Previous Tasks:** T002  
**Next Tasks:** All translation tasks (T018-T039) depend on this
