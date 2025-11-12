# T[NUMBER]: [Subject Name] - Visual Intelligence & Generation
**Stage 4:** Illustration Pipeline  
**Subject:** [Brief 1-line description]  
**Priority:** Critical / High / Medium / Low  
**Source Chapters:** [List chapters where this appears]  
**Ambiguity Score:** [1-10 - how many valid interpretations exist]  
**Spawned By:** T200 Master Orchestrator

---

## Context Requirements

### Required Files
- Chapter(s): [Specific chapter numbers]
- Character perspectives on [subject] from all appearances
- Technical appendices (if applicable)
- Previous illustrations for style consistency
- `Instructions/Illustration-Generation-Guide.md` (style reference)

### Load Strategy
Load only chapters where [subject] appears or is discussed  
Total estimated context: [X]K tokens

---

## Multi-Phase Processing

This ticket executes in 4 sequential phases. **Do not skip phases.**

---

### PHASE 1: Intelligence Gathering
**LLM:** Sonnet 3.5  
**Token Budget:** 200K limit / ~50K required  
**Cost:** $5.00

#### Task: Generate Comprehensive Visual Intelligence Report

Extract and analyze every reference to [subject] across all source material.

#### 1.1 Direct Textual Descriptions

List every explicit description of [subject]:
- Quote from text
- Page/chapter reference
- Which character's perspective
- Context of observation

**Format:**
```markdown
- Ch. [N], p.[X]: "[exact quote]" (Narrator: [character])
  Context: [what was happening when this was observed]
```

#### 1.2 Indirect Evidence

Evidence from character reactions, environmental effects, comparative descriptions:
- How characters reacted to seeing it
- Physical effects it caused (lighting changes, sound, etc.)
- Comparisons to known objects
- What it did/how it moved

#### 1.3 Contradictions Identified

**CRITICAL SECTION:** Document every contradiction between descriptions:
```markdown
CONTRADICTION #1: [Aspect that differs]
- Character A (Ch.X): "[quote]" → suggests [interpretation]
- Character B (Ch.Y): "[quote]" → suggests [different interpretation]
- Cannot reconcile because: [reason]
```

#### 1.4 Technical Constraints

Physical/biological/engineering limits that must be respected:
- Physics: [what laws apply]
- Biology: [if organic, what constraints]
- Engineering: [if mechanical, what's possible]
- Scale: [size relative to known objects]

#### 1.5 Ambiguity Analysis

**What CANNOT be determined from the text:**
- [ ] Exact dimensions
- [ ] Color/texture
- [ ] Number of components
- [ ] Material composition
- [ ] Orientation/directionality
- [ ] Static vs dynamic features
- [Other unknowables]

**Why these cannot be resolved:**
[Explain why the text is deliberately or accidentally ambiguous here]

#### 1.6 Human Perception Notes

How different characters perceived it differently:
- Why perception varied (stress, lighting, distance, expertise)
- Which perceptions are most reliable
- Whether the [subject] itself changed or perception changed

#### Output: Save Intelligence Report

**File:** `Output/Illustrations/Intelligence/T[NUMBER]-[Subject]-Intelligence.md`

**Quality Check:**
- [ ] All textual references extracted
- [ ] Contradictions clearly documented
- [ ] Ambiguities explicitly identified
- [ ] Technical constraints listed
- [ ] Multiple perspectives captured

---

### PHASE 2: Prompt Generation
**LLM:** Haiku  
**Token Budget:** 200K limit / ~5K required  
**Cost:** $0.25

#### Task: Generate Image Generation Prompts

Using the intelligence report, create prompts for Grok Imagine that:
1. Maintain technical sketch aesthetic
2. Preserve identified ambiguities
3. Include appropriate incompleteness
4. Generate multiple valid interpretations

#### 2.1 Primary Prompt (Maximally Ambiguous)

```
"Technical field sketch, engineering drawing style, pencil on grid paper,
[INSERT SUBJECT WITH ALL CONTRADICTIONS/AMBIGUITIES], multiple overlapping
interpretations visible, measurement annotations with question marks,
erasure marks where artist gave up trying to resolve [SPECIFIC AMBIGUITY],
cold clinical documentation style, incomplete sections at [AREAS THAT
CANNOT BE DETERMINED], annotations reading '[SPECIFIC CONFUSION]',
no emotion, as if drawn by someone who doesn't understand what they're
observing"

NEGATIVE: "no artistic interpretation, no emotion, no manga/anime,
no polished finish, no warmth, no digital art style, no color"
```

#### 2.2 Alternative Interpretation Prompts

Generate 3 alternative prompts emphasizing different valid interpretations:

**Interpretation A:** [First valid reading of contradictions]
```
[Full prompt emphasizing this interpretation]
```

**Interpretation B:** [Second valid reading]
```
[Full prompt emphasizing this interpretation]
```

**Interpretation C:** [Third valid reading or hybrid]
```
[Full prompt emphasizing this interpretation]
```

#### 2.3 Technical Annotations to Include

Visual elements to add to sketch:
- Scale markers: [specific measurements, possibly contradictory]
- Measurement attempts: [dimensions with question marks]
- Annotations: "[specific notes like 'symmetry unclear?' or 'joints impossible?']"
- Arrows pointing to: [features that cannot be resolved]
- Erasure marks at: [areas where comprehension failed]

#### 2.4 Caption Draft (Sarasti-9947 Voice)

```markdown
FIGURE [X.Y]: [SUBJECT] ([STATUS - e.g., "UNRESOLVED", "COMPOSITE", "ATTEMPT N"])

"[Process description - how many iterations, what parameters used, what failed].
[Specific admission - what this particular image cannot determine or resolve].
[Unsettling observation - human response pattern data or philosophical note].
[Optional question - something this image makes the reader consider]."
— Sarasti-9947
```

#### Output: Save Prompt Package

**File:** `Output/Illustrations/Prompts/T[NUMBER]-[Subject]-Prompts.md`

**Quality Check:**
- [ ] Primary prompt incorporates all ambiguities
- [ ] Alternative prompts show valid interpretations
- [ ] Technical annotations specified
- [ ] Caption maintains Sarasti-9947 voice
- [ ] Caption admits specific incomprehension

---

### PHASE 3: Image Generation (Manual Execution)
**Platform:** Grok Imagine (free tier)  
**Cost:** $0.00

#### Task: Generate and Select Images

**This phase is MANUAL** - executed by human using Grok Imagine interface.

#### 3.1 Generation Process

1. **Load prompts** from `Output/Illustrations/Prompts/T[NUMBER]-[Subject]-Prompts.md`

2. **Generate primary interpretation:**
   - Use primary prompt
   - Generate 10-20 variations
   - Save all to temporary folder

3. **Generate alternatives:**
   - Use each alternative prompt
   - Generate 5-10 variations each
   - Save all to temporary folder

4. **Review generation set:**
   - Total of 25-50 candidate images
   - Look for ambiguity preservation
   - Check technical sketch aesthetic
   - Verify incompleteness visible

#### 3.2 Selection Criteria

Select 1-3 final images that:
- [ ] Maximize ambiguity (don't resolve contradictions)
- [ ] Maintain technical drawing style (not artistic)
- [ ] Show appropriate incompleteness (unfinished sections)
- [ ] Include visible annotations (question marks, measurements)
- [ ] Have grid/graph paper background
- [ ] Feel unsettling without being explicit
- [ ] Look like engineering documentation, not art

**If 3 images selected:** Should show maximally different interpretations  
**If 1 image selected:** Should incorporate multiple overlapping interpretations

#### 3.3 Post-Processing

For each selected image:
- [ ] Verify grid paper background present
- [ ] Check that measurement annotations are legible
- [ ] Ensure question marks and erasure marks visible
- [ ] Confirm technical sketch aesthetic (not polished art)
- [ ] Add file metadata: T[NUMBER], [Subject], generation date

#### 3.4 Final Output

**Save to:** `Output/Illustrations/Final/T[NUMBER]-[Subject]-Final-[A/B/C].png`

If multiple images:
- T[NUMBER]-[Subject]-Final-A.png (first interpretation)
- T[NUMBER]-[Subject]-Final-B.png (second interpretation)
- T[NUMBER]-[Subject]-Final-C.png (third interpretation)

**Generation Log:** Document what was tried:
```markdown
## T[NUMBER] Generation Log

**Primary prompt iterations:** [N]
**Alternative prompt iterations:** [N each]
**Total candidates:** [N]
**Selected:** [N] final images
**Selection reasoning:** [Why these specific images]
**Rejected patterns:** [What didn't work and why]
```

**Save log to:** `Output/Illustrations/Final/T[NUMBER]-Generation-Log.md`

---

### PHASE 4: Caption Refinement
**LLM:** Haiku  
**Token Budget:** 200K limit / ~2K required  
**Cost:** $0.10

#### Task: Finalize Caption Based on Actual Generated Image

Review the actual selected image(s) and refine the caption to accurately reflect what was generated.

#### Input Context
- The actual generated image(s)
- Intelligence report (Phase 1 output)
- Draft caption (Phase 2 output)
- Generation log (Phase 3 output)

#### Refinement Criteria

The caption must:
1. **Accurately describe the generation process**
   - Actual number of iterations from log
   - Specific failures encountered
   - What was attempted vs what succeeded

2. **Admit specific incomprehension visible in image**
   - Point to exact features that couldn't be resolved
   - Reference the question marks and annotations present
   - Note which contradictions remain unresolved

3. **Match the actual image's characteristics**
   - If showing overlapping interpretations, mention that
   - If incomplete sections visible, reference them
   - If measurement attempts failed, note that

4. **Maintain perfect Sarasti-9947 voice**
   - Clinical, emotionless
   - Admits processing without understanding
   - May include unsettling observation
   - May pose unanswerable question

#### Example Refinement

**Draft Caption (Phase 2):**
```markdown
FIGURE 5.1: SCRAMBLER MORPHOLOGY (COMPOSITE)

"Generated 47 interpretations. These three maximize variance.
Cannot determine correct version."
```

**Refined Caption (Phase 4 - after seeing actual image):**
```markdown
FIGURE 5.1: SCRAMBLER MORPHOLOGY (UNRESOLVED)

"Drew 47 iterations. None satisfied all parameters. This composite
shows three maximally different interpretations overlaid. The joints
bend at angles I cannot process. The symmetry count varies between
observers. Either the entity exists in superposition until observed,
or human perception cannot accurately record its form. Or both.
73% of test viewers report discomfort. The remaining 27% claim to
see something familiar. I can determine neither comfort nor familiarity."
— Sarasti-9947
```

#### Output: Save Final Caption

**File:** `Output/Illustrations/Captions/T[NUMBER]-[Subject]-Caption.md`

**Format:**
```markdown
# Figure Caption: [SUBJECT]

## For Book Publication

FIGURE [X.Y]: [SUBJECT] ([STATUS])

"[Final refined caption maintaining Sarasti-9947 voice]"
— Sarasti-9947

---

## Image Metadata

- **Ticket:** T[NUMBER]
- **Subject:** [Full subject name]
- **Chapters:** [Source chapters]
- **Image File(s):** [Filenames]
- **Ambiguity Score:** [1-10]
- **Iterations Generated:** [N]
- **Final Selection:** [A/B/C or composite]
- **Generated:** [Date]
- **Caption Finalized:** [Date]
```

**Quality Check:**
- [ ] Caption accurately reflects generated image
- [ ] Specific incomprehensions noted
- [ ] Sarasti-9947 voice maintained perfectly
- [ ] Process description accurate per log
- [ ] Metadata complete

---

## Success Criteria

**Ticket Complete When:**

- [ ] **Phase 1:** Intelligence report comprehensively documents all evidence
- [ ] **Phase 1:** Contradictions explicitly identified
- [ ] **Phase 1:** Ambiguities that cannot be resolved are clear
- [ ] **Phase 2:** Prompts generated for primary + 3 alternatives
- [ ] **Phase 2:** Draft caption in Sarasti-9947 voice
- [ ] **Phase 3:** 1-3 final images selected and saved
- [ ] **Phase 3:** Generation log documents process
- [ ] **Phase 4:** Caption refined to match actual image
- [ ] **All files saved to correct locations with correct naming**

---

## File Output Checklist

Upon completion, these files must exist:

```
Output/Illustrations/Intelligence/T[N]-[Subject]-Intelligence.md
Output/Illustrations/Prompts/T[N]-[Subject]-Prompts.md
Output/Illustrations/Final/T[N]-[Subject]-Final-[A/B/C].png
Output/Illustrations/Final/T[N]-[Subject]-Generation-Log.md
Output/Illustrations/Captions/T[N]-[Subject]-Caption.md
```

---

## Cost Summary

| Phase | LLM | Tokens | Cost |
|-------|-----|--------|------|
| 1. Intelligence | Sonnet 3.5 | 50K | $5.00 |
| 2. Prompts | Haiku | 5K | $0.25 |
| 3. Generation | Grok Imagine | - | $0.00 |
| 4. Caption | Haiku | 2K | $0.10 |
| **Total** | | **57K** | **$5.35** |

---

## Remember

Every illustration is an opportunity to demonstrate that the translator:
- **Processes without seeing** - maps patterns, not mental images
- **Cannot resolve ambiguity** - presents multiple interpretations
- **Admits incomprehension** - openly states what it cannot determine
- **Documents what it cannot understand** - technical precision without meaning

The rougher and more uncertain the sketch, the more effective the philosophical point.

---

**Status:** ⏳ TODO  
**Spawned By:** T200 (Master Orchestrator)  
**Blocks:** Final book compilation (needs all images complete)
