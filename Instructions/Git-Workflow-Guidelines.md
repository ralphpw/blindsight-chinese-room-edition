# Git Workflow Guidelines
## Instructions for Version Control Strategy

This project uses Git to create a transparent, educational record of the translation process.

---

## Philosophy

**Preserve what matters, squash what doesn't:**
- Show the **real work**: review iterations and quality refinement
- Hide the noise: research deliverables are just outputs, not process
- Create educational timeline showing **how quality emerges**
- Maintain reproducibility at each stage

**Most Important to Preserve:** Review cycle iterations - this is where the translation becomes good, and researchers need to see this process.

---

## Branch Strategy

### Main Branch
**Purpose:** Clean, public-facing history

**What goes here:**
- Completed stages (Research → Summaries → Translation → Reviews → Publication)
- Major milestones
- Final outputs
- Documentation updates

**What doesn't:**
- Work-in-progress iterations
- Failed attempts
- Experimental approaches
- Minor fixes during active work

### Working Branch: `translation-wip`
**Purpose:** All active translation work

**What goes here:**
- Individual chapter translations as they're completed
- Review iterations
- Consistency fixes
- Experimental changes

**Merge to main:** Only after stage completion with squash

---

## Commit Strategy by Stage

### Stage 0: Project Setup
**Commits to Keep (main):**
```
✅ Initial commit: Project structure and documentation
✅ Add Instructions folder and ticket templates
✅ Add all 60 task tickets
✅ Complete project documentation
```

**Branch:** Commit directly to `main`  
**Why:** Setup is one-time, foundational, educational

---

### Stage 1: Research (T001-T013)
**Commits to Keep (main):**
```
✅ Stage 1 complete: Research phase
```

**Branch:** Work in `translation-wip`, merge to `main` with **SQUASH**

**Why:**
- Research outputs are just deliverables, not an evolving process
- Character studies don't iterate - they're generated once
- Jargon dictionary is final output, not gradual refinement
- Researchers care about **what** was produced, not intermediate steps

**Git commands:**
```bash
# Working
git checkout -b translation-wip
git add Tasks/01-Research/source-material/*.md
git commit -m "T001-T002: Add source material"
git add Tasks/01-Research/character-studies/*.md
git commit -m "T003-T007: Character studies complete"
git add Tasks/01-Research/dialogue-extraction/*.md
git commit -m "T008-T012: Dialogue banks extracted"
git add Tasks/01-Research/jargon-analysis/*.md
git commit -m "T013: Jargon dictionary complete"

# When stage complete, SQUASH merge
git checkout main
git merge --squash translation-wip
git commit -m "Stage 1 complete: Research phase

Deliverables:
- Source material converted to 22 Markdown chapters
- 5 character studies (Keeton, Sarasti, Szpindel, Bates, Cunningham)
- 5 dialogue banks extracted per character
- Comprehensive jargon dictionary (200+ terms)

LLMs used: Claude Opus 3.5, Haiku 3.5, GPT-4o
Cost: $25-30, Time: 2-3 weeks"

git branch -D translation-wip
```

---

### Stage 2: Summaries (T014-T017)
**Commits to Keep (main):**
```
✅ T014-T015: Add chapter summaries (all 22)
✅ T016-T017: Add character snapshots (all 22)
✅ Stage 2 complete: Summaries phase
```

**Branch:** Work in `translation-wip`, merge to `main` with **squash**

**Why:**
- Summaries are preparatory, not final output
- 22 individual chapter summary commits = noise
- One "summaries complete" commit sufficient
- Researchers care about output, not granular process here

**Git commands:**
```bash
# Working
git checkout translation-wip
git add Tasks/02-Summaries/chapter-summaries/*.md
git commit -m "T014: Chapters 1-11 summaries"
git add Tasks/02-Summaries/character-snapshots/*.md
git commit -m "T016: Character snapshots 1-11"

# When stage complete, squash merge
git checkout main
git merge --squash translation-wip
git commit -m "Stage 2 complete: Chapter summaries and character snapshots

- 22 chapter summaries (Sonnet)
- 22 character snapshot sets (GPT-4o-mini)
- Preparatory context for translation phase"
git branch -D translation-wip
git checkout -b translation-wip  # Fresh branch for next stage
```

---

### Stage 3: Translation (T018-T039)
**Commits to Keep (main):**
```
✅ T018: Chapter 1 translated (FOUNDATION - Opus)
✅ Chapters 2-22 translated
✅ Stage 3 complete: Translation phase
```

**Branch:** Work in `translation-wip`, merge to `main` with **partial squash**

**Strategy:**
- **Preserve:** Chapter 1 (foundational, Opus, critical)
- **Squash:** Chapters 2-22 into one commit
- **Why:** Chapter 1 establishes voice (educational value), rest is iteration

**Git commands:**
```bash
# Chapter 1 (preserve)
git checkout translation-wip
git add Tasks/03-Translation/chapters/chapter-01-translated.md
git commit -m "T018: Chapter 1 translated (Opus - voice foundation)

First chapter sets tone and establishes character voices.
Premium Opus model used for quality.
Cost: $10, Time: 6 hours"

# Merge Ch 1 to main immediately
git checkout main
git merge --no-ff translation-wip -m "Chapter 1 complete: Translation voice established"
git checkout translation-wip

# Chapters 2-22 (squash later)
for i in {2..22}; do
  git add Tasks/03-Translation/chapters/chapter-0${i}-translated.md
  git commit -m "T0XX: Chapter $i translated"
done

# When all chapters done, squash merge
git checkout main
git merge --squash translation-wip
git commit -m "Chapters 2-22 translated (Sonnet + selective Opus)

- 18 standard chapters (Sonnet, $2 each)
- 3 critical chapters (Opus, $7-10 each: Ch 4, 12, 20)
- Consistent voice maintained from Chapter 1
- Total cost: $66, Time: 3-4 months

Translation phase complete."
```

---

### Stage 4: Reviews (T040-T047) ⭐ MOST IMPORTANT
**Commits to Keep (main):**
```
✅ ALL REVIEW ITERATIONS - PRESERVE EVERYTHING
✅ Initial review reports
✅ Every fix applied
✅ Each review cycle
✅ Final sign-off
```

**Branch:** Work in `translation-wip`, merge to `main` with **NO SQUASH - PRESERVE ALL COMMITS**

**Why This Is Critical:**
- ⭐ **This shows the REAL work** of making the translation good
- Review iterations demonstrate quality emergence through refinement
- Most educational part of entire project
- Shows how LLM+human collaboration improves output
- Demonstrates methodology in action (not just results)
- Researchers need to see: problem found → fix applied → verification

**Git commands:**
```bash
# DO NOT SQUASH - Each commit tells the story of refinement
git checkout translation-wip

# Review 1: Scientific Accuracy
git add Tasks/04-Reviews/scientific-accuracy-report.md
git commit -m "T040: Scientific accuracy review complete (GPT-4o)

Issues found: 12 neuroscience terms, 3 physics concepts
Critical: 5, Moderate: 7, Minor: 3"

git add Tasks/03-Translation/chapters/chapter-07-translated.md
git commit -m "Fix: Ch 7 neuroscience terminology (synaptic → neural connections)

Changed 'synaptic topology' to consistent 'how neurons connect'
per jargon dictionary. Critical fix from scientific review."

git add Tasks/03-Translation/chapters/chapter-12-translated.md
git commit -m "Fix: Ch 12 consciousness explanation (scientific accuracy)

Simplified 'phenomenological binding' to 'how experiences feel unified'
without losing technical accuracy. Moderate priority from T040."

# Review 2: Internal Consistency
git add Tasks/04-Reviews/consistency-report.md
git commit -m "T041: Internal consistency review complete (Sonnet)

Cross-chapter analysis found:
- 8 jargon inconsistencies
- 3 character voice variations
- 2 recurring phrase mismatches"

git add Tasks/03-Translation/chapters/chapter-05-translated.md
git commit -m "Fix: Ch 5 Sarasti voice (removed contraction 'don't')

Sarasti uses 'do not' - no contractions ever.
Character consistency issue from T041."

git add Tasks/03-Translation/chapters/chapter-09-translated.md
git add Tasks/03-Translation/chapters/chapter-14-translated.md
git commit -m "Fix: Ch 9, 14 jargon consistency ('vampire' biology)

Standardized crucifix glitch description across chapters.
Both now match Ch 3 phrasing per consistency review."

# Review 3: Plot Integrity
git add Tasks/04-Reviews/plot-integrity-report.md
git commit -m "T042: Plot integrity review complete (Gemini)

All plot beats preserved from original.
No translation-introduced contradictions found.
Timeline references verified consistent."

# Review 4: Beta Reads
git add Tasks/04-Reviews/beta-read-feedback-1.md
git commit -m "T044: Beta read #1 feedback received

Reader feedback: Ch 16 too technical, Ch 19 Keeton voice wavers
Actionable items: 3 critical, 5 moderate"

git add Tasks/03-Translation/chapters/chapter-16-translated.md
git commit -m "Fix: Ch 16 accessibility (beta reader feedback)

Simplified quantum physics explanation without dumbing down.
Reader reported 'lost the thread' - now clearer."

git add Tasks/03-Translation/chapters/chapter-19-translated.md
git commit -m "Fix: Ch 19 Keeton voice consistency (beta feedback)

Keeton narration became too clinical. Restored introspective,
relatable tone consistent with Ch 1 voice foundation."

# Final validation
git add Tasks/04-Reviews/final-editorial-pass.md
git commit -m "T047: Final editorial pass complete (human)

All critical issues resolved.
Moderate issues reviewed - 8 applied, 2 deferred as stylistic.
Minor polish applied throughout.

✅ Translation ready for publication."

# Merge to main PRESERVING ALL COMMITS
git checkout main
git merge --no-ff translation-wip -m "Stage 4 complete: Review cycles with all iterations preserved

This merge preserves the complete review refinement process:
- Scientific accuracy fixes (neuroscience, physics)
- Character voice consistency (esp. Sarasti)
- Jargon standardization across 22 chapters
- Beta reader feedback integration
- Final editorial validation

See individual commits for detailed evolution of quality."
```

**Result:** Git history shows **HOW** the translation got good, not just that it is good.

---

### Stage 5: Publication (T048-T060)
**Commits to Keep (main):**
```
✅ T048-T052: Add appendices
✅ T053-T054: Add formatted outputs (PDF, EPUB)
✅ T055-T056: Publish to platforms
✅ RELEASE: v1.0 - The Sarasti Translation
```

**Branch:** Work in `translation-wip`, merge to `main` with **individual commits preserved**

**Why:**
- Publication steps are final, polished deliverables
- Each appendix is meaningful contribution
- Format outputs (PDF/EPUB) are important milestones
- Researchers want to see final assembly process

**Git commands:**
```bash
# Individual commits preserved
git checkout translation-wip
git add Tasks/05-Publication/appendices/appendix-a-philosophy.md
git commit -m "T049: Add Appendix A - Translation Philosophy"

git add Tasks/05-Publication/appendices/appendix-d-reproducibility.md
git commit -m "T050: Add Appendix D - Reproducibility (with repo links)"

git add Tasks/05-Publication/outputs/blindsight-sarasti-translation.pdf
git commit -m "T053: Generate PDF output (Pandoc)"

git add Tasks/05-Publication/outputs/blindsight-sarasti-translation.epub
git commit -m "T054: Generate EPUB output (Calibre)"

# Merge preserving history
git checkout main
git merge --no-ff translation-wip -m "Stage 5 complete: Publication phase"

# Tag release
git tag -a v1.0 -m "Release: Blindsight - The Sarasti Translation v1.0

22 chapters translated for accessibility
Appendices with methodology and reproducibility info
PDF and EPUB formats
Published to AO3 and GitHub

Licensed under CC BY-NC-SA 4.0"
git push origin v1.0
```

---

## Summary: What Gets Squashed vs. Preserved

| Stage | Strategy | Rationale |
|-------|----------|-----------|
| **Setup** | Squash to 1-2 commits | Just infrastructure, not interesting |
| **Stage 1: Research** | **SQUASH** | Just deliverables (character studies, jargon dict) - outputs, not process |
| **Stage 2: Summaries** | **SQUASH** | Preparatory work, not final output |
| **Stage 3: Translation** | **SQUASH except Ch 1** | Ch 1 is foundational (voice), rest pre-review is just first draft |
| **Stage 4: Reviews** | **PRESERVE ALL** | ⭐ **MOST IMPORTANT** - Shows how quality emerges through iteration |
| **Stage 5: Publication** | **PRESERVE** | Each appendix is unique and educational |

**Key Insight:** The review iterations are the most educational part - preserve them to show the real work of refining quality.

---

## Git History Visualization

**Result on `main` branch:**
```
* v1.0 - Release: Blindsight - The Sarasti Translation v1.0
* T054: Generate EPUB output (Calibre)
* T053: Generate PDF output (Pandoc)
* T052: Add Appendix C - Jargon Guide
* T051: Add Appendix B - From Sarasti
* T050: Add Appendix D - Reproducibility
* T049: Add Appendix A - Translation Philosophy
* T047: Final editorial pass complete ✅
* Fix: Ch 19 Keeton voice (beta feedback)
* Fix: Ch 16 accessibility (beta feedback)
* T044: Beta read #1 feedback received
* T042: Plot integrity review complete
* Fix: Ch 9, 14 jargon consistency
* Fix: Ch 5 Sarasti voice (removed contraction)
* T041: Internal consistency review complete
* Fix: Ch 12 consciousness explanation (scientific)
* Fix: Ch 7 neuroscience terminology (synaptic)
* T040: Scientific accuracy review complete
* Chapters 2-22 translated (pre-review draft)
* Chapter 1 translated (voice foundation - Opus)
* Stage 2 complete: Summaries phase
* Stage 1 complete: Research phase
* Project setup: Documentation and tickets
* Initial commit
```

**Shows the real work: Review iterations preserved** ⭐ **Most educational commits**

---

## Special Commits

### Documentation Updates
**Strategy:** Commit directly to `main` as they happen

```bash
git checkout main
git add Documentation/AI-Reviews.md
git commit -m "docs: Add AI review guidelines and examples"
git add Instructions/Consistency-Review-Guidelines.md
git commit -m "docs: Add internal consistency review process"
```

**Why:** Documentation changes are meta-work, not translation work

### Bug Fixes Post-Publication
**Strategy:** Fix in `main`, tag new version

```bash
git checkout main
git add Tasks/03-Translation/chapters/chapter-07-translated.md
git commit -m "fix: Correct neuroscience term in Chapter 7 (typo)"
git tag -a v1.0.1 -m "Patch: Fix Chapter 7 neuroscience typo"
```

---

## .gitignore Recommendations

```gitignore
# Temporary work files
*.tmp
*~
.DS_Store

# LLM iteration drafts (don't commit until final)
*-draft-*.md
*-attempt-*.md

# Local build artifacts
*.aux
*.log
*.out

# But DO commit:
# - All markdown outputs
# - PDF/EPUB finals
# - All instruction files
# - All tickets
# - All documentation
```

---

## Benefits of This Strategy

### For Transparency
- ✅ Researchers see **HOW** quality emerges (not just final state)
- ✅ Review iterations show real refinement process
- ✅ Methodology visible through commit messages

### For Education
- ⭐ **Review commits are case studies** in LLM quality improvement
- ✅ Students can trace: problem → fix → validation
- ✅ Shows LLM+human collaboration in action
- ✅ Demonstrates iterative refinement methodology

### For Reproducibility
- ✅ Each stage has clear commit
- ✅ Can checkout pre-review state and re-run reviews
- ✅ Version tags for releases
- ✅ Diff between review cycles shows exactly what changed

### For the Meta-Irony
- ✅ Translation "source code" is public
- ✅ Git history shows Chinese Room executing, then **being corrected**
- ✅ Review commits show **human oversight of non-conscious process**
- ✅ Perfect demonstration: LLMs execute, humans validate

**The review commits are the most valuable educational artifact in the entire repository.**

---

## Implementation: Update Ticket T050

Add git workflow to reproducibility appendix:
- Link to commit history
- Explain why certain stages squashed
- Show how researchers can explore timeline

---

*This file should be referenced by all stage completion tasks (T013, T017, T039, T047, T060).*
