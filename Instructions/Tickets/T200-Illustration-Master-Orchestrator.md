# T200: Illustration Master Orchestrator
**Stage 3:** Illustration Pipeline - Master Identification  
**LLM:** Sonnet (orchestration logic required)  
**Token Budget:** 200K limit / ~80K required  
**Estimated Cost:** $8.00  
**Dependencies:** All chapter translations complete (T006-T027)

---

## Purpose

Scan all 22 chapters to identify illustration candidates and automatically generate individual processing tickets (T201-T299) for each image to be created.

This is a **meta-ticket** that spawns worker tickets. Do not generate images directly.

---

## Context Requirements

### Required Files
- All completed chapter translations (T006-T027 outputs)
- `Instructions/Illustration-Generation-Guide.md` (selection criteria)
- `Instructions/TEMPLATE.md` (ticket structure)

### Load Strategy
- Read chapters sequentially (don't load all at once)
- Extract image candidates as you scan
- Generate tickets in batches

---

## Task Instructions

### Phase 1: Scan Each Chapter for Candidates

For chapters 01-22, identify illustration opportunities using criteria from `Illustration-Generation-Guide.md`:

**Priority 1: Maximum Horror Potential (CRITICAL)**
- Ambiguous entities that defy comprehension (Scramblers, Rorschach interior)
- The uncanny valley moments (Sarasti's "wrongness," vampire predator reveals)
- Scenes where reality becomes unreliable (impossible geometries, phase-shifted entities)
- The incomprehensible attempting to communicate (The Conversation scene)
- Body horror or violation of expected forms (joints bending wrong, too many angles)
- Moments where consciousness itself is questioned (Gang of Four switching, Siri's blindsight episodes)

**Priority 2: Disturbing Technical Details**
- Vampire neurology (predator brain with visible differences)
- Crucifix glitch pattern (with explicit warning - may induce discomfort)
- Non-Euclidean ship architecture (spaces that shouldn't connect)
- Interface technology violating bodily autonomy
- Failed attempts to diagram the incomprehensible

**Priority 3: Isolation and Scale Horror**
- The vast emptiness of deep space (emphasize insignificance)
- Rorschach's alien scale (overwhelming, incomprehensible size)
- Theseus alone in the void (existential dread)
- Earth's distant irrelevance (abandonment)
- The Oort cloud's cold indifference

**Priority 4: Character Horror Studies**
- Sarasti's face showing multiple conflicting interpretations (predator vs human)
- Characters under extreme stress (emotional breakdown visualized)
- Physical transformations that disturb (Gang switching, augmentation reveals)
- The moment someone realizes they're not conscious (philosophical horror)

### Phase 2: Validate Against Criteria

For each candidate, ask:
1. **Horror Effectiveness (1-10):** How unsettling/disturbing is this image likely to be?
2. **Ambiguity Score (1-10):** How many valid interpretations exist?
3. **Reader Impact:** Does this enhance the psychological horror experience?
4. **Chinese Room Horror Synergy:** Does the translator's incomprehension make this MORE disturbing?
5. **Budget Justification:** Worth $5.35 in processing costs?

Reject:
- Clear action scenes (reader imagination better)
- Purely informational diagrams without horror element
- Simple objects adequately described
- Redundant visualizations
- Anything that diminishes horror through clarity

### Phase 3: Generate Worker Tickets

For each approved candidate, create a ticket following this template:

```markdown
# T[NUMBER]: [Subject] Visual Intelligence & Generation
**Stage 3:** Illustration Pipeline  
**Subject:** [Brief description]  
**Priority:** Critical/High/Medium/Low  
**Source Chapters:** [List all chapters mentioning this subject]  
**Ambiguity Score:** [1-10]

---

## Context Requirements

- Chapters: [specific chapters]
- Character perspectives on [subject]
- Technical appendices (if applicable)
- Previous illustrations for consistency

---

## Multi-Phase Process

### Phase 1: Intelligence Gathering (Sonnet, ~50K tokens, $5)

Generate comprehensive visual intelligence report:

#### 1.1 Direct Textual Descriptions
[Extract every description of subject across all chapters]

#### 1.2 Indirect Evidence
[Character reactions, environmental effects, comparative descriptions]

#### 1.3 Contradictions Identified
[List conflicting descriptions with page references]

#### 1.4 Technical Constraints
[Physics, biology, engineering limits that must be respected]

#### 1.5 Ambiguity Analysis
[What CANNOT be determined from text]

#### 1.6 Human Perception Notes
[How different characters perceived it differently]

**Output:** Save to `Output/Illustrations/Intelligence/T[N]-[Subject]-Intelligence.md`

---

### Phase 2: Prompt Generation (Haiku, ~5K tokens, $0.25)

Using intelligence report, generate:

#### 2.1 Primary Prompt (Maximally Ambiguous)
```
"Technical field sketch, pencil on grid paper, [detailed subject description
incorporating all uncertainty and contradictions], multiple overlapping 
interpretations, measurement annotations with question marks, erasure marks,
incomplete sections, cold clinical documentation style, no emotion"
```

#### 2.2 Alternative Interpretations
1. [Organic interpretation prompt]
2. [Mechanical interpretation prompt]
3. [Hybrid interpretation prompt]

#### 2.3 Technical Annotations to Include
- Scale markers (possibly inconsistent)
- Measurement attempts (contradictory if ambiguous)
- Question marks at unresolved features
- "Unable to resolve" notes

#### 2.4 Caption Draft (Sarasti-9947 Voice)
```markdown
FIGURE [X.Y]: [SUBJECT] ([INTERPRETATION STATUS])

"[Process description: how many iterations, what failed]. 
[Admission of incomprehension: what cannot be determined].
[Unsettling observation: human response data or philosophical note].
[Optional: unanswerable question to reader]."
— Sarasti-9947
```

**Output:** Save to `Output/Illustrations/Prompts/T[N]-[Subject]-Prompts.md`

---

### Phase 3: Image Generation Instructions (Manual Step)

**Platform:** Grok Imagine (free tier)

#### 3.1 Generation Process
1. Use primary prompt to generate 10-20 variations
2. Use alternative prompts to generate 5-10 each
3. Select 1-3 that maximize ambiguity and maintain technical sketch aesthetic
4. Verify grid paper background, annotations, incompleteness

#### 3.2 Selection Criteria
- Maximum ambiguity preserved
- Technical drawing style maintained
- Appropriate incompleteness visible
- Unsettling without being explicit
- Question marks and annotations legible

#### 3.3 Post-Processing
- Ensure grid/graph paper background
- Add measurement lines if missing
- Verify technical sketch aesthetic
- Check that incompleteness is visible

**Output:** Save selected image(s) to `Output/Illustrations/Final/T[N]-[Subject]-Final.png`

---

### Phase 4: Final Caption Generation (Haiku, ~2K tokens, $0.10)

Review final selected image(s) and refine caption to match what was actually generated:

```markdown
FIGURE [X.Y]: [SUBJECT] ([STATUS])

"[Accurate process description based on actual iterations].
[Specific admission of what the final image cannot resolve].
[Observation about this particular rendering].
[Question that this specific image raises]."
— Sarasti-9947
```

**Output:** Save to `Output/Illustrations/Captions/T[N]-[Subject]-Caption.md`

---

## Success Criteria

- [ ] Intelligence report comprehensively covers all textual evidence
- [ ] Contradictions clearly identified
- [ ] Prompts maintain technical sketch style requirements
- [ ] Caption maintains perfect Sarasti-9947 voice
- [ ] All outputs saved to correct file locations
- [ ] Image selection maximizes ambiguity appropriately

---

## Cost Breakdown

- Intelligence Gathering: $5.00 (Sonnet, 50K tokens)
- Prompt Generation: $0.25 (Haiku, 5K tokens)
- Caption Refinement: $0.10 (Haiku, 2K tokens)
- Image Generation: $0.00 (Grok Imagine free tier)

**Total per illustration:** ~$5.35

---

## Notes

This is a **complex multi-phase ticket**. Each phase builds on the previous:
1. Intelligence → 2. Prompts → 3. Images (manual) → 4. Captions

Do not skip intelligence gathering. The ambiguity analysis is critical for maintaining the Chinese Room philosophical consistency.
```

Save each ticket as `Instructions/T[NUMBER]-[Subject-Name].md`

### Phase 4: Generate Manifest

Create `Output/Illustrations/MANIFEST.md`:

```markdown
# Illustration Manifest
Generated: [Date]
Total Candidates: [N]

## By Priority

### Critical (Must Have)
- T[N]: [Subject] - [Chapter(s)] - Ambiguity: [Score]/10
[...]

### High (Strong Value)
- T[N]: [Subject] - [Chapter(s)] - Ambiguity: [Score]/10
[...]

### Medium (Nice to Have)
- T[N]: [Subject] - [Chapter(s)] - Ambiguity: [Score]/10
[...]

### Low (If Budget Allows)
- T[N]: [Subject] - [Chapter(s)] - Ambiguity: [Score]/10
[...]

## By Type

### Technical Diagrams ([N])
[List]

### Ambiguous Entities ([N])
[List]

### Character Studies ([N])
[List]

### Atmospheric ([N])
[List]

## Budget Summary

Total Illustrations: [N]
Estimated Cost: $[N × 5.35]
Timeline: [N ÷ 3 per day] = [X] days
```

---

## Output Requirements

### 1. Individual Ticket Files
Create `Instructions/T[201-299]-*.md` for each approved candidate

### 2. Manifest File
Create `Output/Illustrations/MANIFEST.md` with complete listing

### 3. Summary Report
Generate `Output/Illustrations/T200-Orchestration-Report.md`:

```markdown
# T200 Orchestration Report

## Chapters Scanned
22/22 complete

## Candidates Identified
- Total found: [N]
- Approved: [N]
- Rejected: [N]

## Rejection Reasons
- Adequately described in text: [N]
- Redundant with other images: [N]
- Inappropriate for Chinese Room: [N]
- Low reader value: [N]

## Tickets Generated
T201-T[N]: [N total tickets]

## Estimated Resources
- Total cost: $[N × 5.35]
- Total time: [N ÷ 3 per day] days
- Token usage: [estimate]

## Priority Distribution
- Critical: [N] (~$[cost])
- High: [N] (~$[cost])
- Medium: [N] (~$[cost])
- Low: [N] (~$[cost])

## Recommendations
1. Execute Critical priority first (test pipeline)
2. Hold Medium/Low pending budget review
3. [Other recommendations]
```

---

## Execution Strategy

1. **Start:** Load Chapter 01, scan for candidates
2. **Iterate:** For each chapter, identify 1-3 high-value images
3. **Generate:** Create ticket file for each approved candidate
4. **Document:** Update manifest as you progress
5. **Report:** Final summary with recommendations

**Target:** 25-35 total illustrations (avg 1-2 per chapter)  
**Budget:** $135-190 total ($5.35 per image)  
**Timeline:** 2-3 weeks (3-4 images per day)

---

## Quality Criteria

Each generated ticket must:
- [ ] Include specific chapter references
- [ ] List all textual evidence locations
- [ ] Define clear ambiguity preservation requirements
- [ ] Provide cost breakdown
- [ ] Include success criteria checklist

---

## Remember

You are identifying where the Chinese Room's pattern-mapping will fail most interestingly **and most disturbingly**. Look for:
- **Contradictions it cannot resolve** (multiple nightmare interpretations)
- **Ambiguities that terrify** (what IS that thing?)
- **Visualizations it cannot comprehend** (impossible geometries, phase-shifted entities)
- **The uncanny valley of failed understanding** (almost human, almost comprehensible, but WRONG)

Every illustration is an opportunity to demonstrate processing without understanding **while maximizing psychological horror**. The translator's incomprehension should make the horror worse, not better.

**The perfect image:** Multiple overlapping interpretations, all disturbing, none fully comprehensible, with annotations showing where the pattern-matching broke down trying to process something that shouldn't exist.

---

**Status:** ⏳ TODO  
**Blocking:** None (can start immediately after chapter translations)  
**Blocks:** All T201-T299 illustration tickets
