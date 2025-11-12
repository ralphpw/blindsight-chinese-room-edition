# T050: Attribution and Reproducibility Appendix

**Stage:** 5-Publication  
**Status:** TODO  
**LLM:** Human + Haiku  
**Estimated Cost:** $0.50  
**Estimated Time:** 2 hours  
**Depends On:** T048, T049

---

## Context Requirements

**Documents to Read BEFORE Starting:**

- [ ] `Instructions/Reproducibility-Guidelines.md` - GitHub permalink strategy and Appendix D template
- [ ] `Instructions/Git-Workflow-Guidelines.md` - Understanding what commits to preserve/reference
- [ ] `Documentation/Legal-Framework.md` - Copyright and attribution requirements
- [ ] Git commit history (actual commits, not just tickets)

**Critical:** Need access to actual git history and commit SHAs for accurate permalinks.

---

## Objective

Create comprehensive attribution appendix linking to exact GitHub repo version and instruction files used, ensuring full transparency and reproducibility.

---

## Process

### 1. Capture Repository State (Human)

**At publication time, record:**
- GitHub repository URL
- Specific commit SHA (exact version used)
- Date of publication
- Branch name (likely `main`)

**Command:**
```bash
git log -1 --format="%H %ci" > repo-version.txt
```

### 2. Generate Appendix (Haiku)

Create appendix section with:
- Link to GitHub repo
- Commit SHA and date
- Links to specific instruction files at that commit
- Version of each LLM used
- List of all instruction files referenced

### 3. Add to Final Manuscript

Insert as **Appendix D: Reproducibility** after:
- Appendix A: Translation Philosophy
- Appendix B: From Sarasti
- Appendix C: Jargon Guide

---

## Inputs Required

- [ ] Final GitHub repository URL
- [ ] Commit SHA at publication time
- [ ] List of all instruction files used
- [ ] LLM versions used (Claude 3.5 Sonnet build date, etc.)

---

## Outputs

```
Tasks/05-Publication/appendices/
└── appendix-d-reproducibility.md
```

**Expected Length:** 2-3 pages  
**Expected Format:** Markdown with clickable GitHub links

---

## Required Content

### GitHub Links Section
```markdown
## Source Code and Instructions

This translation was produced using the following instruction set:

**Repository:** https://github.com/[username]/blindsight-chinese-room-edition  
**Release:** v1.0 (Commit: [SHA], [Date])  
**Branch:** main

### Instruction Files Used

All instruction files are preserved at the above release tag:

- [AI Review Guidelines](https://github.com/.../Instructions/AI-Review-Guidelines.md)
- [Character Voice Profiles](https://github.com/.../Instructions/Prompts/character-voice-*.md)
- [System Prompt](https://github.com/.../Instructions/Prompts/system-prompt-base.md)
- [Jargon Dictionary](https://github.com/.../Tasks/01-Research/jargon-analysis/jargon-dictionary.md)
- [All 60 Task Tickets](https://github.com/.../Instructions/Tickets/)

### Git History

Explore the translation process through commit history:

- [Stage 1: Research](https://github.com/.../commits/main?since=[date]&until=[date])
- [Stage 2: Summaries](https://github.com/.../commits/main?since=[date]&until=[date])
- [Stage 3: Translation](https://github.com/.../commits/main?since=[date]&until=[date])
- [Stage 4: Reviews](https://github.com/.../commits/main?since=[date]&until=[date])
- [Stage 5: Publication](https://github.com/.../commits/main?since=[date]&until=[date])

**Note:** Some stages squashed for clarity. See [Git Workflow Guidelines](Instructions/Git-Workflow-Guidelines.md) for rationale.
```

### LLM Versions Section
```markdown
## AI Models Used

- **Primary Translation:** Claude 3.5 Sonnet (Anthropic, build date: [date])
- **Character Studies:** Claude Opus 3.5 (Anthropic, build date: [date])
- **Reviews:** GPT-4o, Gemini 1.5 Pro, Perplexity (versions as of [date])
- **Extraction:** Claude Haiku 3.5 (Anthropic, build date: [date])
```

### Reproducibility Statement
```markdown
## How to Reproduce This Translation

Anyone can reproduce this translation process:

1. Clone the repository at the specified commit
2. Acquire *Blindsight* source material (free from rifters.com)
3. Follow tickets T001-T060 in sequence
4. Use the same LLM models with specified configurations
5. Compare your output to this published version

**Note:** Due to LLM non-determinism, results will be similar but not identical.
```

---

## Quality Gates

- [ ] Repository URL is public and accessible
- [ ] Commit SHA is locked (will never change)
- [ ] All instruction file links work (use permalink format)
- [ ] LLM versions are specific (build dates, not just model names)
- [ ] Reproducibility instructions are clear and complete
- [ ] Appendix fits book formatting standards

---

## LLM Configuration

**Model:** Claude Haiku 3.5  
**Why:** Simple formatting task, low cost  
**Context:** Repo state, LLM versions list  
**Temperature:** 0.1 (precise, factual)

**Prompt:**
```markdown
Create Appendix D: Reproducibility for the Blindsight translation.

INPUTS:
- Repository: [URL]
- Commit: [SHA] on [Date]
- LLMs used: [list with versions]
- Instruction files: [list from repo]

FORMAT: Professional appendix following academic standards.

REQUIREMENTS:
- All GitHub links use permalink format (include commit SHA in URL)
- Clear reproducibility instructions
- Complete attribution of tools and methods
- 2-3 pages maximum

OUTPUT: Markdown formatted appendix ready for inclusion in book.
```

---

## GitHub Permalink Format

**Standard link (changes):**  
`https://github.com/user/repo/blob/main/file.md`

**Permalink (permanent):**  
`https://github.com/user/repo/blob/[commit-SHA]/file.md`

**Always use permalinks in the appendix.**

---

## Success Criteria

This appendix ensures:
1. **Full Transparency**: Readers see exact instructions used
2. **Reproducibility**: Anyone can recreate the process
3. **Academic Rigor**: Proper attribution of tools and methods
4. **Future-Proof**: Links work even if repo changes
5. **Meta-Irony**: Book literally points to its own "source code"

---

## Notes

- This is unique in literary translation (pointing to GitHub instructions)
- Reinforces the "open source translation" philosophy
- Allows researchers to study the methodology
- Creates accountability (instructions are public, locked to version)
- Perfect meta-commentary: "Here are the Chinese Room instructions I followed"

**This appendix IS the translation's citation.**

---

**Previous Task:** T049 (Appendix A - Translation Philosophy)  
**Next Task:** T051 (Appendix C - Jargon Guide)
