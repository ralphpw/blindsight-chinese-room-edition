# Blindsight: The Sarasti Translation
## Complete Project Structure

---

## Overview

This document defines the complete folder structure for the LLM-driven translation project, organized into **sequential workflow stages** for automated processing by long-running AI agents (Cursor, GitHub Copilot, etc.).

---

## Root Folder Structure

```
blindsight-sarasti-translation/
│
├── 00-Project-Docs/              # Human-readable project documentation
│   ├── README.md
│   ├── Project-Overview.md
│   ├── Legal-Framework.md
│   ├── Character-Philosophy.md
│   ├── Technical-Approach.md
│   ├── Audience-Analysis.md
│   └── Publication-Strategy.md
│
├── 01-Research/                  # Foundation phase (deep analysis)
│   ├── README.md                 # Phase 1 overview
│   ├── source-material/
│   │   ├── chapter-01-original.md
│   │   ├── chapter-02-original.md
│   │   └── ... (22 chapters)
│   ├── character-studies/
│   │   ├── keeton-deep-dive.md
│   │   ├── sarasti-deep-dive.md
│   │   ├── szpindel-deep-dive.md
│   │   ├── bates-deep-dive.md
│   │   └── cunningham-deep-dive.md
│   ├── dialogue-extraction/
│   │   ├── keeton-all-dialogue.md
│   │   ├── sarasti-all-dialogue.md
│   │   ├── szpindel-all-dialogue.md
│   │   ├── bates-all-dialogue.md
│   │   └── cunningham-all-dialogue.md
│   ├── jargon-analysis/
│   │   ├── jargon-dictionary.md
│   │   ├── neuroscience-terms.md
│   │   ├── physics-terms.md
│   │   └── watts-neologisms.md
│   └── progress.md               # Research phase status tracking
│
├── 02-Summaries/                 # Story context & character states
│   ├── README.md                 # Phase 2 overview
│   ├── chapter-summaries/
│   │   ├── chapter-01-summary.md
│   │   ├── chapter-02-summary.md
│   │   └── ... (22 chapters)
│   ├── character-snapshots/
│   │   ├── chapter-01-states.md
│   │   ├── chapter-02-states.md
│   │   └── ... (22 chapters - evolving states)
│   ├── theme-tracking/
│   │   ├── chinese-room-instances.md
│   │   ├── consciousness-debates.md
│   │   └── vampire-science.md
│   └── progress.md               # Summary phase status tracking
│
├── 03-Translation/               # Chapter-by-chapter translation
│   ├── README.md                 # Phase 3 overview
│   ├── prompts/
│   │   ├── system-prompt-base.md
│   │   ├── character-voice-keeton.md
│   │   ├── character-voice-sarasti.md
│   │   ├── character-voice-szpindel.md
│   │   ├── character-voice-bates.md
│   │   ├── character-voice-cunningham.md
│   │   └── chapter-template.md
│   ├── chapters/
│   │   ├── chapter-01-translated.md
│   │   ├── chapter-02-translated.md
│   │   └── ... (22 chapters)
│   ├── change-logs/
│   │   ├── chapter-01-changes.md
│   │   ├── chapter-02-changes.md
│   │   └── ... (what changed and why)
│   └── progress.md               # Translation status tracking
│
├── 04-Reviews/                   # Quality control & validation
│   ├── README.md                 # Phase 4 overview
│   ├── llm-reviews/
│   │   ├── claude-opus-review.md
│   │   ├── gpt4-review.md
│   │   ├── gemini-review.md
│   │   └── consolidated-feedback.md
│   ├── human-reviews/
│   │   ├── scientific-accuracy-check.md
│   │   ├── continuity-check.md
│   │   └── beta-reader-feedback.md
│   ├── revisions/
│   │   ├── revision-log.md
│   │   └── issues-resolved.md
│   └── progress.md               # Review phase status tracking
│
├── 05-Publication/               # Final outputs & distribution
│   ├── README.md                 # Phase 5 overview
│   ├── manuscript/
│   │   ├── 00-preface.md
│   │   ├── 01-chapter-01.md
│   │   ├── 02-chapter-02.md
│   │   └── ... (compiled for PDF generation)
│   ├── appendices/
│   │   ├── appendix-A-system-prompt.md
│   │   ├── appendix-B-methodology.md
│   │   ├── appendix-C-what-changed.md
│   │   └── appendix-D-ai-reviews.md
│   ├── formats/
│   │   ├── Blindsight-Sarasti-Translation-2025.pdf
│   │   ├── Blindsight-Sarasti-Translation-2025.epub
│   │   └── Blindsight-Sarasti-Translation-2025.mobi
│   ├── release-notes.md
│   └── progress.md               # Publication status tracking
│
├── 90-Kanban/                    # Task management (LLM-executable)
│   ├── README.md                 # Kanban board status
│   ├── backlog/
│   ├── in-progress/
│   ├── review/
│   ├── done/
│   └── templates/
│       └── task-template.md
│
└── 99-Archive/                   # Deprecated or experimental files
    ├── experiments/
    ├── old-versions/
    └── notes/
```

---

## Workflow Stages (Sequential Processing)

### **Stage 1: Research (01-Research/)**

**Purpose:** Deep analysis and data extraction before any translation begins

**LLM Recommendations:**
- **Claude Opus 3.5** for character studies (best at nuanced analysis, $15/1M input)
- **Claude Haiku 3.5** for dialogue extraction (fast, cheap bulk processing, $0.80/1M input)
- **GPT-4o** for jargon analysis (strong with technical terms, $2.50/1M input)

**Tasks:**
1. Download and convert *Blindsight* to Markdown (22 chapters)
2. Extract ALL dialogue per character (dialogue-extraction/)
3. Generate comprehensive character studies (character-studies/)
4. Build jargon dictionary (jargon-analysis/)

**Output Quality Gates:**
- [ ] All 22 chapters in clean Markdown
- [ ] 5 character deep-dives (1500+ lines each)
- [ ] 5 dialogue banks (every line extracted)
- [ ] Jargon dictionary (200+ terms mapped)

**Estimated Time:** 2-3 weeks  
**Estimated Cost:** $20-30 (mostly Opus for deep analysis)

---

### **Stage 2: Summaries (02-Summaries/)**

**Purpose:** Story context and evolving character mental states

**LLM Recommendations:**
- **Claude Sonnet 3.5** for chapter summaries (balanced quality/cost, $3/1M input)
- **Claude Sonnet 3.5** for character snapshots (requires nuanced understanding)
- **GPT-4o-mini** for theme tracking (fast pattern recognition, $0.15/1M input)

**Tasks:**
1. Summarize each chapter (plot, themes, tone)
2. Create character state snapshots per chapter (method acting reference)
3. Track recurring themes (Chinese Room instances, consciousness debates)

**Output Quality Gates:**
- [ ] 22 chapter summaries (plot, characters, concepts)
- [ ] 22 character snapshot files (mental/emotional states)
- [ ] Theme tracking complete (cross-references)

**Estimated Time:** 1-2 weeks  
**Estimated Cost:** $10-15 (Sonnet for quality, mini for bulk)

---

### **Stage 3: Translation (03-Translation/)**

**Purpose:** Chapter-by-chapter translation with state-aware character voices

**LLM Recommendations:**
- **Claude Sonnet 3.5** for primary translation (best prose quality, $3/1M input, $15/1M output)
- **Alternative: Claude Opus 3.5** for critical chapters (higher quality, 5x cost)
- **Avoid: Haiku** (too fast, loses nuance in creative work)

**Cost/Quality Trade-offs:**

| Model | Input Cost | Output Cost | Speed | Quality | Best For |
|-------|-----------|-------------|-------|---------|----------|
| **Opus 3.5** | $15/1M | $75/1M | Slow | Highest | Critical chapters (1, 10, 22) |
| **Sonnet 3.5** | $3/1M | $15/1M | Medium | High | Standard chapters (bulk) |
| **Haiku 3.5** | $0.80/1M | $4/1M | Fast | Medium | NOT recommended for prose |

**Recommended Approach:**
- **Chapters 1, 10, 15, 22** → Opus (critical narrative moments)
- **All other chapters** → Sonnet (consistent quality, cost-effective)
- **Total Cost:** ~$40-60 for full novel

**Tasks per Chapter:**
1. Load context (original, snapshot, summary, jargon dict)
2. Execute translation with system prompt
3. Human review (scientific accuracy only)
4. Update next chapter's character snapshots
5. Document major changes (change-logs/)

**Output Quality Gates:**
- [ ] 22 translated chapters
- [ ] Character voices distinct and consistent
- [ ] All jargon translated per dictionary
- [ ] Scientific accuracy preserved
- [ ] Atmosphere intact

**Estimated Time:** 3-6 months (one chapter per weekend)  
**Estimated Cost:** $40-60 (Sonnet primary, Opus for critical)

---

### **Stage 4: Reviews (04-Reviews/)**

**Purpose:** Multi-LLM quality validation and human scientific accuracy check

**LLM Recommendations:**
- **Claude Opus 3.5** for comprehensive review (best analytical depth)
- **GPT-4o** for alternative perspective (different training, catches different issues)
- **Gemini 1.5 Pro** for scientific fact-checking (strong technical knowledge, $1.25/1M input)
- **Perplexity** for neuroscience validation (web search + LLM combo)

**Tasks:**
1. Submit full manuscript to 3+ different LLMs
2. Request: voice consistency, scientific accuracy, thematic preservation
3. Consolidate feedback (llm-reviews/consolidated-feedback.md)
4. Human scientific accuracy pass (neuroscience, physics)
5. Address critical issues (revisions/)
6. Beta reader feedback (human-reviews/)

**Output Quality Gates:**
- [ ] 3+ LLM reviews completed
- [ ] Scientific accuracy validated
- [ ] Continuity issues resolved
- [ ] Beta reader feedback incorporated

**Estimated Time:** 1-2 months  
**Estimated Cost:** $20-30 (multiple full-manuscript reads)

---

### **Stage 5: Publication (05-Publication/)**

**Purpose:** Format conversion, final compilation, distribution

**LLM Recommendations:**
- **Claude Haiku 3.5** for formatting cleanup (fast, cheap, $0.80/1M)
- **GPT-4o** for metadata generation (titles, descriptions, SEO)
- **Human tools:** Pandoc (Markdown → PDF), Calibre (EPUB validation)

**Tasks:**
1. Compile all chapters into manuscript/ folder
2. Add preface (Sarasti's Translator's Note)
3. Add appendices (system prompt, methodology, reviews)
4. Convert to PDF, EPUB, MOBI (Pandoc, Calibre)
5. Generate release notes
6. Publish to AO3, GitHub, website

**Output Quality Gates:**
- [ ] Professional PDF formatting
- [ ] Valid EPUB (passes Calibre check)
- [ ] All appendices included
- [ ] Legal notices on every platform
- [ ] Download links active

**Estimated Time:** 2-4 weeks  
**Estimated Cost:** $5-10 (minimal LLM use, mostly tooling)

---

## LLM Model Selection Guide

### **Claude (Anthropic) Family**

#### **Opus 3.5** - Premium Tier
- **Cost:** $15/1M input, $75/1M output
- **Speed:** Slow (highest latency)
- **Quality:** Best prose, deepest analysis
- **Use For:**
  - Character deep-dives (Stage 1)
  - Critical chapter translations (1, 10, 22)
  - Comprehensive final review (Stage 4)
- **Avoid For:** Bulk processing, time-sensitive tasks

#### **Sonnet 3.5** - Balanced Tier ⭐ Primary Workhorse
- **Cost:** $3/1M input, $15/1M output
- **Speed:** Medium (good balance)
- **Quality:** High (best value)
- **Use For:**
  - Chapter summaries (Stage 2)
  - Character snapshots (Stage 2)
  - Most chapter translations (Stage 3)
  - Initial reviews (Stage 4)
- **Avoid For:** Simple formatting tasks (use Haiku)

#### **Haiku 3.5** - Economy Tier
- **Cost:** $0.80/1M input, $4/1M output
- **Speed:** Fast (lowest latency)
- **Quality:** Medium (good enough for simple tasks)
- **Use For:**
  - Dialogue extraction (Stage 1)
  - Formatting cleanup (Stage 5)
  - Metadata generation
- **Avoid For:** Creative prose, nuanced analysis

---

### **OpenAI Family**

#### **GPT-4o** - Premium Alternative
- **Cost:** $2.50/1M input, $10/1M output
- **Speed:** Fast (faster than Claude Sonnet)
- **Quality:** High (different style than Claude)
- **Use For:**
  - Jargon analysis (Stage 1)
  - Alternative review perspective (Stage 4)
  - Technical fact-checking
- **Avoid For:** Primary prose (Claude better for literary work)

#### **GPT-4o-mini** - Economy Alternative
- **Cost:** $0.15/1M input, $0.60/1M output
- **Speed:** Very fast
- **Quality:** Medium (good for patterns)
- **Use For:**
  - Theme tracking (Stage 2)
  - Bulk pattern recognition
  - Simple data extraction
- **Avoid For:** Anything requiring creativity or nuance

---

### **Google Gemini**

#### **Gemini 1.5 Pro**
- **Cost:** $1.25/1M input, $5/1M output
- **Speed:** Fast
- **Quality:** High technical accuracy
- **Use For:**
  - Scientific fact-checking (Stage 4)
  - Physics/neuroscience validation
  - Alternative review
- **Avoid For:** Creative prose (tends to be verbose)

---

### **Perplexity**

#### **Perplexity Pro**
- **Cost:** $20/month subscription (unlimited)
- **Speed:** Medium
- **Quality:** High for factual accuracy (web search + LLM)
- **Use For:**
  - Neuroscience validation (Stage 4)
  - Fact-checking Watts' science
  - Research validation
- **Avoid For:** Creative work, bulk processing

---

## Cost Breakdown by Stage

### **Optimized Budget (Recommended)**

| Stage | Primary LLM | Cost Estimate | Rationale |
|-------|-------------|---------------|-----------|
| **1. Research** | Opus (studies) + Haiku (extraction) | $20-30 | Deep analysis where it matters |
| **2. Summaries** | Sonnet (all) + GPT-4o-mini (themes) | $10-15 | Balanced quality/cost |
| **3. Translation** | Sonnet (18 ch) + Opus (4 ch) | $40-60 | Premium for critical chapters |
| **4. Reviews** | Opus + GPT-4o + Gemini | $20-30 | Multiple perspectives |
| **5. Publication** | Haiku (cleanup) + tools | $5-10 | Minimal LLM needed |
| **TOTAL** | Mixed strategy | **$95-145** | Full novel translation |

### **Premium Budget (Highest Quality)**

| Stage | Primary LLM | Cost Estimate | Rationale |
|-------|-------------|---------------|-----------|
| **1. Research** | Opus (all) | $40-50 | Best analysis across the board |
| **2. Summaries** | Opus (all) | $25-35 | Deepest understanding |
| **3. Translation** | Opus (all 22 chapters) | $150-200 | Maximum prose quality |
| **4. Reviews** | Opus + GPT-4o + Gemini + Perplexity | $40-50 | Exhaustive validation |
| **5. Publication** | Sonnet (polish) | $10-15 | Professional finish |
| **TOTAL** | Opus-heavy | **$265-350** | Premium quality throughout |

### **Economy Budget (Minimum Viable)**

| Stage | Primary LLM | Cost Estimate | Rationale |
|-------|-------------|---------------|-----------|
| **1. Research** | Sonnet (all) | $10-15 | Good enough for foundation |
| **2. Summaries** | GPT-4o-mini (all) | $3-5 | Fast pattern work |
| **3. Translation** | Sonnet (all) | $25-35 | Consistent baseline |
| **4. Reviews** | GPT-4o + Gemini | $10-15 | Two perspectives |
| **5. Publication** | Haiku (all) | $2-5 | Minimal processing |
| **TOTAL** | Budget-focused | **$50-75** | Acceptable quality, tight budget |

---

## Automation Strategy for Long-Running Agents

### **Cursor / GitHub Copilot Workflow**

#### **Stage-by-Stage Execution**

```python
# Pseudocode for automated workflow

def execute_stage_1_research():
    """Stage 1: Research - Deep analysis"""
    llm_config = {
        'character_studies': 'claude-opus-3.5',  # Best analysis
        'dialogue_extraction': 'claude-haiku-3.5',  # Fast bulk
        'jargon_analysis': 'gpt-4o'  # Technical terms
    }
    
    for task in research_tasks:
        select_llm(llm_config[task.type])
        execute_task(task)
        validate_output(task.quality_gates)
        update_progress('01-Research/progress.md')

def execute_stage_2_summaries():
    """Stage 2: Summaries - Context building"""
    llm_config = {
        'chapter_summaries': 'claude-sonnet-3.5',  # Balanced
        'character_snapshots': 'claude-sonnet-3.5',  # Nuanced
        'theme_tracking': 'gpt-4o-mini'  # Fast patterns
    }
    
    for chapter in range(1, 23):
        generate_summary(chapter, llm_config)
        generate_snapshots(chapter, llm_config)
        update_progress('02-Summaries/progress.md')

def execute_stage_3_translation():
    """Stage 3: Translation - Chapter by chapter"""
    llm_config = {
        'critical_chapters': [1, 10, 15, 22],  # Opus for these
        'standard_chapters': range(2, 23),  # Sonnet for rest
    }
    
    for chapter in range(1, 23):
        if chapter in llm_config['critical_chapters']:
            llm = 'claude-opus-3.5'  # Premium quality
        else:
            llm = 'claude-sonnet-3.5'  # Standard quality
        
        context = load_context(chapter)
        translation = translate_chapter(chapter, llm, context)
        human_review_scientific_accuracy(translation)
        update_character_snapshots(chapter + 1)
        update_progress('03-Translation/progress.md')

def execute_stage_4_reviews():
    """Stage 4: Reviews - Quality validation"""
    llm_config = {
        'comprehensive': 'claude-opus-3.5',
        'alternative': 'gpt-4o',
        'scientific': 'gemini-1.5-pro',
        'fact_check': 'perplexity'
    }
    
    manuscript = compile_manuscript()
    
    for llm_name, llm_model in llm_config.items():
        review = request_review(manuscript, llm_model)
        save_review(f'04-Reviews/llm-reviews/{llm_name}-review.md')
    
    consolidate_feedback()
    address_critical_issues()
    update_progress('04-Reviews/progress.md')

def execute_stage_5_publication():
    """Stage 5: Publication - Final outputs"""
    compile_manuscript_with_appendices()
    generate_pdf('pandoc')  # Human tool
    generate_epub('calibre')  # Human tool
    cleanup_formatting('claude-haiku-3.5')  # Cheap LLM
    publish_to_platforms()
    update_progress('05-Publication/progress.md')

# Main execution
if __name__ == '__main__':
    execute_stage_1_research()
    execute_stage_2_summaries()
    execute_stage_3_translation()
    execute_stage_4_reviews()
    execute_stage_5_publication()
```

---

### **Progress Tracking per Stage**

Each stage folder includes `progress.md`:

```markdown
# Stage 1: Research - Progress Tracking

**Started:** 2025-01-15  
**Target Completion:** 2025-02-05  
**Status:** IN PROGRESS

## Tasks

| Task | Status | LLM Used | Cost | Started | Completed |
|------|--------|----------|------|---------|-----------|
| Download source | ✅ DONE | Human | $0 | 2025-01-15 | 2025-01-15 |
| Character studies | 🔄 IN PROGRESS | Opus | $15 | 2025-01-16 | - |
| Dialogue extraction | ⏳ TODO | Haiku | $5 | - | - |
| Jargon dictionary | ⏳ TODO | GPT-4o | $10 | - | - |

## Quality Gates

- [x] All 22 chapters in Markdown
- [ ] 5 character deep-dives (1500+ lines each)
- [ ] 5 dialogue banks (every line extracted)
- [ ] Jargon dictionary (200+ terms)

## Issues / Blockers

- None currently

## Next Steps

1. Complete Keeton character study (Opus, est. 2 hours)
2. Begin Sarasti character study
3. ...
```

---

## Kanban Integration (90-Kanban/)

### **Folder Structure**

```
90-Kanban/
├── README.md (board status overview)
├── backlog/
│   ├── task-001-download-source.md
│   ├── task-002-keeton-study.md
│   └── ... (all 30+ tasks)
├── in-progress/
│   └── (tasks move here when started)
├── review/
│   └── (tasks move here when awaiting validation)
├── done/
│   └── (completed tasks archived here)
└── templates/
    └── task-template.md
```

### **Task Template**

```markdown
# Task XXX: [Task Name]

**Stage:** [1-Research | 2-Summaries | 3-Translation | 4-Reviews | 5-Publication]  
**Status:** [BACKLOG | IN PROGRESS | REVIEW | DONE]  
**LLM:** [Opus | Sonnet | Haiku | GPT-4o | etc.]  
**Estimated Cost:** $X  
**Estimated Time:** X hours  
**Depends On:** [Task IDs]

## Objective
[Clear description]

## Inputs Required
- File A
- File B

## Process
1. Step 1
2. Step 2

## Outputs
- File X (in folder Y)

## Quality Gates
- [ ] Criterion 1
- [ ] Criterion 2

## Execution Notes
[LLM-specific instructions]

---
**Started:** [Date]  
**Completed:** [Date]  
**Actual Cost:** $X  
**Issues:** [Any problems encountered]
```

---

## Final Directory Tree

```
blindsight-sarasti-translation/
│
├── 00-Project-Docs/              # ← Human documentation
├── 01-Research/                  # ← Stage 1 (Opus + Haiku + GPT-4o)
├── 02-Summaries/                 # ← Stage 2 (Sonnet + GPT-4o-mini)
├── 03-Translation/               # ← Stage 3 (Sonnet + Opus for critical)
├── 04-Reviews/                   # ← Stage 4 (Multi-LLM validation)
├── 05-Publication/               # ← Stage 5 (Haiku + human tools)
├── 90-Kanban/                    # ← Task tracking
└── 99-Archive/                   # ← Old versions, experiments
```

---

**This structure enables:**
- ✅ Clear sequential workflow (1→2→3→4→5)
- ✅ Cost optimization (right LLM for each task)
- ✅ Progress tracking per stage
- ✅ Automated agent execution (Cursor/Copilot friendly)
- ✅ Quality gates at each stage
- ✅ Transparent methodology

---

*Document Version: 2.0*  
*Last Updated: January 2025*  
*Includes: LLM model selection, cost optimization, automation strategy*
