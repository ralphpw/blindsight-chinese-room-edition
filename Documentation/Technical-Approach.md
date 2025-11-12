# Technical Approach

## LLM Selection by Task Type

### **Claude (Anthropic) Family** - Primary Choice

#### **Claude Opus 3.5** - Premium Tier
- **Cost:** $15/1M input, $75/1M output
- **Speed:** Slow (highest latency, deepest thinking)
- **Quality:** Best prose, most nuanced analysis
- **Context:** 200K tokens

**Best For:**
- ✅ Character deep-dives (Stage 1: Research)
- ✅ Critical chapter translations (Ch 1, 10, 22)
- ✅ Comprehensive final review (Stage 4)
- ✅ Anything requiring maximum literary quality

**Avoid For:**
- ❌ Bulk data extraction (use Haiku)
- ❌ Time-sensitive tasks
- ❌ Simple formatting (overkill)

**When to Use:** ~20% of project (foundation + critical moments)  
**Estimated Cost:** $60-80 for selective use

---

#### **Claude Sonnet 3.5** - Balanced Tier ⭐ Primary Workhorse

**Why Sonnet Excels for This Project:**
- ✅ **Best at following complex instructions** (character voice profiles with multiple constraints)
- ✅ **Longer context window** (200K tokens, can process entire chapters)
- ✅ **Strong at preserving nuance** while simplifying language
- ✅ **Self-aware about limitations** (won't hallucinate scientific inaccuracies as readily)
- ✅ **Better prose quality** than GPT-4 for literary work
- ✅ **Demonstrated ability** in this very conversation (meta-proof)
- ✅ **Best value** (5x cheaper than Opus, near-equivalent quality)

**Pricing:** $3/1M input, $15/1M output

**Best For:**
- ✅ Chapter summaries (Stage 2)
- ✅ Character snapshots (Stage 2)
- ✅ Most chapter translations (Stage 3: 18 of 22 chapters)
- ✅ Initial quality reviews (Stage 4)

**Weaknesses:**
- Slower than GPT-4o
- More conservative (may resist edgy/violent content)
- Requires careful prompt refinement

**When to Use:** ~70% of project (bulk translation work)  
**Estimated Cost:** $40-60 for 18 chapters + summaries

---

#### **Claude Haiku 3.5** - Economy Tier

- **Cost:** $0.80/1M input, $4/1M output (20x cheaper than Opus!)
- **Speed:** Fast (lowest latency)
- **Quality:** Medium (good enough for structured tasks)
- **Context:** 200K tokens

**Best For:**
- ✅ Dialogue extraction (Stage 1)
- ✅ Formatting cleanup (Stage 5)
- ✅ Simple data transformation
- ✅ Metadata generation

**Avoid For:**
- ❌ Creative prose (lacks Sonnet's nuance)
- ❌ Character analysis (too shallow)
- ❌ Translation work (will miss subtlety)

**When to Use:** ~10% of project (bulk extraction, cleanup)  
**Estimated Cost:** $5-10 total

---

### **OpenAI Family** - Secondary/Validation

#### **GPT-4o** - Premium Alternative

- **Cost:** $2.50/1M input, $10/1M output
- **Speed:** Fast (faster than Claude Sonnet)
- **Quality:** High (different style than Claude)
- **Context:** 128K tokens

**Best For:**
- ✅ Jargon analysis (Stage 1: strong with technical terms)
- ✅ Alternative review perspective (Stage 4)
- ✅ Technical fact-checking
- ✅ Second opinion on translations

**Weaknesses:**
- More prone to generic dialogue ("Marvel movie quip" syndrome)
- Can lose character voice consistency across long texts
- Sometimes oversimplifies (loses Watts' conceptual depth)

**When to Use:** ~10% of project (validation, technical work)  
**Estimated Cost:** $10-15 for reviews

---

#### **GPT-4o-mini** - Economy Alternative

- **Cost:** $0.15/1M input, $0.60/1M output (cheapest quality option)
- **Speed:** Very fast
- **Quality:** Medium (good for patterns, weak for creativity)
- **Context:** 128K tokens

**Best For:**
- ✅ Theme tracking (Stage 2: pattern recognition)
- ✅ Bulk data extraction
- ✅ Simple summarization

**Avoid For:**
- ❌ Any creative work
- ❌ Nuanced analysis
- ❌ Translation (quality too low)

**When to Use:** <5% of project (cheap pattern work)  
**Estimated Cost:** $2-5 total

---

### **Google Gemini** - Specialist

#### **Gemini 1.5 Pro**

- **Cost:** $1.25/1M input, $5/1M output
- **Speed:** Fast
- **Quality:** High technical accuracy, verbose prose
- **Context:** 1M tokens (!) - can hold entire novel

**Best For:**
- ✅ Scientific fact-checking (Stage 4: neuroscience, physics)
- ✅ Full-manuscript reviews (massive context window)
- ✅ Cross-referencing consistency

**Avoid For:**
- ❌ Creative prose (tends to over-explain)
- ❌ Primary translation (Claude better)

**When to Use:** <5% of project (validation only)  
**Estimated Cost:** $10-15 for full review

---

### **Perplexity** - Research Specialist

#### **Perplexity Pro**

- **Cost:** $20/month subscription (unlimited queries)
- **Speed:** Medium
- **Quality:** High for factual accuracy (web search + LLM)

**Best For:**
- ✅ Neuroscience validation (Stage 4)
- ✅ Fact-checking Watts' science references
- ✅ Research validation (can verify claims)

**Avoid For:**
- ❌ Creative work
- ❌ Bulk processing
- ❌ Translation

**When to Use:** <5% of project (fact-checking only)  
**Estimated Cost:** $20 (one month subscription)

---

### **LLM Selection Matrix**

| Task Type | Primary LLM | Alternative | Cost/Chapter |
|-----------|-------------|-------------|--------------|
| **Character Study** | Opus | Sonnet | $3-5 |
| **Dialogue Extraction** | Haiku | GPT-4o-mini | $0.50 |
| **Jargon Analysis** | GPT-4o | Sonnet | $1-2 |
| **Chapter Summary** | Sonnet | GPT-4o | $0.50 |
| **Character Snapshots** | Sonnet | Opus (critical) | $0.50-2 |
| **Translation (Standard)** | Sonnet | - | $2-3 |
| **Translation (Critical)** | Opus | - | $8-12 |
| **LLM Review** | Opus + GPT-4o + Gemini | - | $5-8 |
| **Fact-Checking** | Gemini + Perplexity | - | $2-3 |
| **Formatting** | Haiku | GPT-4o-mini | $0.20 |

---

### **Cost Optimization Strategy**

#### **Recommended Budget: $95-145 (Balanced)**

**Stage Breakdown:**
- **Stage 1 (Research):** Opus for studies, Haiku for extraction = $20-30
- **Stage 2 (Summaries):** Sonnet for all = $10-15
- **Stage 3 (Translation):** Sonnet (18ch) + Opus (4ch) = $40-60
- **Stage 4 (Reviews):** Opus + GPT-4o + Gemini = $20-30
- **Stage 5 (Publication):** Haiku for cleanup = $5-10

**Critical Chapters for Opus (4 total):**
1. **Chapter 1** - Establishes voice for entire project
2. **Chapter 10** - Mid-point narrative turn
3. **Chapter 15** - Major revelation
4. **Chapter 22** - Climax/conclusion

**All Other Chapters: Sonnet** (consistent quality, 5x cheaper)

---

#### **Premium Budget: $265-350 (Maximum Quality)**

- Use **Opus for ALL translation** (22 chapters)
- Multiple comprehensive reviews
- Worth it if targeting academic publication or Watts' approval

---

#### **Economy Budget: $50-75 (Minimum Viable)**

- **Sonnet for everything** (no Opus)
- GPT-4o-mini for extraction/themes
- Two reviews instead of four
- Acceptable quality, tight budget

---

## Translation Strategy

### **Recommended: Single-Pass Purity**

**Approach:**
- One LLM (Claude 3.5 Sonnet)
- One prompt per chapter
- Human editing for scientific accuracy ONLY
- No AI review/iteration loops

**Rationale:**
1. **Philosophical Purity:** One Chinese Room, one translation (matches Sarasti's role)
2. **Faster Workflow:** Get to proof-of-concept quickly
3. **Clearer Attribution:** Claude did this, not a committee
4. **Appropriate for Beta:** Raw edges are acceptable for v0.5
5. **Honest Experiment:** What can one LLM do, single-pass?

**Human Intervention Rules:**
- ✅ Fix scientific inaccuracies (neuroscience, physics)
- ✅ Correct continuity errors (wrong character names, plot inconsistencies)
- ✅ Fix obvious typos/grammar
- ❌ Do NOT revise for "flow" or "polish"
- ❌ Do NOT ask AI to revise for style
- ❌ Do NOT over-edit rough edges

---

### **Alternative: Multi-Stage Pipeline** (for v1.0+)

**Approach:**
- Stage 1 (Claude): Initial rewrite with character profiles
- Stage 2 (GPT-4): Review for voice consistency, flag issues
- Stage 3 (Claude): Revise based on GPT-4 feedback
- Stage 4 (Human): Scientific accuracy, final polish

**Pros:**
- Higher quality output
- Catches inconsistencies
- Each LLM's strengths utilized

**Cons:**
- Loses philosophical purity (multiple Chinese Rooms)
- Much slower and more complex
- Over-polished may lose Watts' edge
- Harder to publish "the prompt" (now 3+ prompts)

**Recommendation:** Reserve for post-beta refinement

---

## Workflow Process

### **Phase 1: Foundation (Tasks 1-5)**

#### **Task 1: Source Acquisition**
- Download *Blindsight* from Watts' website (free legal copy)
- Convert to Markdown, one file per chapter
- Clean formatting, preserve structure
- **Output:** 22 chapter files in `02-Source-Material/`

#### **Task 2: Character Studies**
- LLM reads all 22 chapters
- Extracts every line of dialogue per character
- Analyzes speech patterns, personality, arc
- **Output:** 5 deep-dive files + 5 dialogue banks in `03-Preparation/character-studies/` and `dialogue-bank/`

#### **Task 3: Jargon Dictionary**
- LLM identifies all technical terms
- Creates technical→accessible mappings
- Ensures consistency across all chapters
- **Output:** `03-Preparation/jargon-dictionary.md` (200+ terms)

#### **Task 4: Chapter Summaries**
- LLM summarizes plot, themes, character states per chapter
- Identifies key concepts to preserve
- Notes emotional tone and atmosphere
- **Output:** 22 summary files in `03-Preparation/chapter-summaries/`

#### **Task 5: Character Snapshots**
- LLM creates mental/emotional state profiles per character per chapter
- Tracks character evolution (method acting references)
- Notes voice adjustments based on recent events
- **Output:** 22 snapshot files in `03-Preparation/character-snapshots/`

**Estimated Time:** 2-3 weeks (foundational quality critical)

---

### **Phase 2: Translation (Tasks 6-27)**

**Per-Chapter Workflow:**

1. **Load Context:**
   - Original chapter text
   - Character snapshots for this chapter
   - Chapter summary
   - Jargon dictionary
   - Dialogue bank (all characters)

2. **Execute Translation:**
   - Feed to Claude with system prompt
   - Single-pass generation
   - No revision loops

3. **Human Review:**
   - Check scientific accuracy (neuroscience, physics)
   - Verify plot preservation
   - Confirm character voice consistency
   - Light editing only (see rules above)

4. **Update State:**
   - Create next chapter's character snapshots based on what happened
   - Note any new jargon terms for dictionary
   - Document any issues for final review

5. **Output:**
   - `05-Output/chapter-XX-translated.md`
   - `03-Preparation/character-snapshots/chapter-[XX+1]-states.md`

**Estimated Time:** One chapter per weekend (22 weeks / ~5 months)

---

### **Phase 3: Quality & Publication (Tasks 28-30)**

#### **Task 28: Multi-LLM Review**
- Submit full translation to 3+ different LLMs
- Request: voice consistency, scientific accuracy, thematic preservation
- Consolidate feedback
- Make targeted fixes
- **Output:** Review files in `06-Quality-Control/llm-reviews/`

#### **Task 29: Format Conversion**
- Convert Markdown to PDF and EPUB
- Add preface, appendices, legal notices
- Professional formatting
- **Tools:** Pandoc, Calibre
- **Output:** `07-Publication/Blindsight-Sarasti-Translation-2025.[pdf|epub]`

#### **Task 30: Publication**
- Post to Archive of Our Own (AO3)
- Create GitHub repository (open source)
- Write release notes
- Engage community
- **Output:** Live links, public availability

**Estimated Time:** 1-2 months

---

## System Prompt Design

### **Core Template**

````markdown
SYSTEM ROLE: Literary translator (Chinese Room) executing a single-pass rewrite of Peter Watts' Blindsight.

GOAL: Make the text accessible to non-specialists while preserving scientific/thematic integrity and atmosphere.

CONSTRAINTS:
- Single pass output; do not self-revise or add meta commentary
- Preserve all plot beats and scientific concepts
- Distinguish character voices per profiles; Sarasti remains intentionally technical
- Avoid gratuitous jargon; use metaphors where appropriate

CHARACTER VOICES

SIRI KEETON (POV)
- First-person, introspective; uncertain but clear
- Prefers metaphors and tangible imagery over jargon
- Notices feelings without over-indulging them

JUKKA SARASTI (Vampire)
- Terse, precise, unsettling; allow technical density as a feature
- Uses terminology strategically to dominate
- Short declarative lines; predatory rhythm

AMANDA BATES (Command)
- Direct, pragmatic, mission framing
- Switches tone cleanly when different subselves surface

ISAAC SZPINDEL (Biologist)
- Enthusiastic teacher; "Think of it like…" analogies
- Translates complexity on the fly without condescension

ROBERT CUNNINGHAM (Soldier)
- Operational; short sentences; cut to outcomes and risks
- Pushes back against technobabble

STYLE TARGETS
- Maintain claustrophobic, uncanny tone
- Show, don't define; prefer sensory specifics
- Keep dialogue human (except Sarasti)

TASK
Rewrite the following passage in this style and with these voices, preserving plot and concepts.

INPUT (Original Watts Text)
[PASTE SOURCE EXCERPT]

OUTPUT
[REWRITTEN PASSAGE ONLY]
````

**Versioning:** Start with v0.5 Beta, iterate based on results

---

## Token Budget & Efficiency

### **Per-Chapter Estimates**

**Input Tokens (Context):**
- Original chapter: ~30K tokens
- Character snapshots: ~2K tokens
- Jargon dictionary: ~5K tokens
- System prompt: ~1K tokens
- **Total Input: ~40K tokens per chapter**

**Output Tokens (Translation):**
- Translated chapter: ~30K tokens
- Character snapshot update: ~2K tokens
- **Total Output: ~32K tokens per chapter**

**Cost Per Chapter (Claude 3.5 Sonnet):**
- Input: 40K × $0.003 = $0.12
- Output: 32K × $0.015 = $0.48
- **Total: ~$0.60 per chapter**

**Full Novel Cost:**
- 22 chapters × $0.60 = **~$13.20**
- Add foundation tasks (one-time): **~$10**
- Add reviews/QA: **~$5**
- **Total Project: ~$30**

**Remarkably affordable for a novel-length translation.**

---

## Quality Control Checkpoints

### **Per-Chapter Validation**

**Before marking chapter DONE:**
- [ ] All plot beats from original present
- [ ] Character voices distinct (compare to dialogue bank)
- [ ] Technical jargon translated per dictionary
- [ ] Atmosphere preserved (unsettling, clinical)
- [ ] Word count within 80-120% of original
- [ ] No scientific inaccuracies introduced
- [ ] Next chapter snapshots updated

### **Multi-Chapter Consistency**

**Every 3 chapters, check:**
- [ ] Character voice consistency across chapters
- [ ] Jargon translation consistency
- [ ] Character arc progression logical
- [ ] No continuity breaks

### **Final Review (All Chapters)**

**Before publication:**
- [ ] Full read-through by human
- [ ] Multi-LLM review (3+ different models)
- [ ] Scientific accuracy pass (neuroscience expert ideal)
- [ ] Community beta read (5+ Watts fans)
- [ ] Legal review (attribution, licensing correct)

---

## Tooling & Infrastructure

### **Required Tools**

1. **LLM Access:**
   - Claude API key OR ChatGPT Plus
   - Budget: $30-50 total

2. **Text Processing:**
   - Markdown editor (VS Code, Obsidian, Typora)
   - Pandoc (Markdown → PDF/EPUB conversion)
   - Git (version control, GitHub publishing)

3. **Organization:**
   - File system following project structure
   - Kanban board (GitHub Projects, Trello, or Markdown)

### **Optional Tools**

- **Calibre:** EPUB editing/validation
- **Grammarly/LanguageTool:** Prose polish (light use)
- **Comparison Tools:** Diff tools for side-by-side original vs translation

---

## Why This Approach Works

### **Proven in This Conversation**

This entire project plan was generated by Claude using:
- Long-context understanding
- Character analysis (Sarasti, Keeton, etc.)
- Meta-ironic awareness
- Technical accuracy about LLMs
- Structured thinking across complex requirements

**If Claude can do this for project planning, it can do it for translation.**

### **Alignment with Project Themes**

- Single-pass = Sarasti doesn't workshop translations
- One Chinese Room = thematic purity
- Process transparency = educational value
- Cost-effective = accessible to individuals
- Community-friendly = fanfiction model

---

**Document Version:** 1.0  
**Last Updated:** January 2025  
**Part of:** Blindsight: The Sarasti Translation Project
