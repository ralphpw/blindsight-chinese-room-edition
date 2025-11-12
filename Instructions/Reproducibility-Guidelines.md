# Reproducibility and Attribution Guidelines
## Instructions for LLMs

All published materials must include links to the exact GitHub repository version and instruction files used.

---

## Core Principle

**Transparency = Trust**

Every output of this project should allow readers to:
1. See the exact instructions that produced it
2. Reproduce the process if desired
3. Verify the methodology claims

---

## Required Attribution Elements

### 1. Repository Reference

**Format:**
```markdown
**Translation Repository:** https://github.com/[username]/blindsight-chinese-room-edition  
**Version:** [commit-SHA] ([date])
```

**Where to Include:**
- Book copyright page
- Appendix D: Reproducibility
- GitHub README
- AO3 metadata/notes
- Any publication of excerpts

### 2. Instruction File Links

**Use GitHub Permalinks (include commit SHA):**

✅ **Correct:**  
`https://github.com/user/repo/blob/abc123def456/Instructions/AI-Review-Guidelines.md`

❌ **Wrong:**  
`https://github.com/user/repo/blob/main/Instructions/AI-Review-Guidelines.md`

**Why:** Main branch changes. Permalink is permanent to that specific version.

### 3. LLM Versions

**Be Specific:**
- ✅ "Claude 3.5 Sonnet (build date: 2024-10-22)"
- ❌ "Claude 3.5"

**Why:** Model capabilities change. Build date ensures reproducibility context.

---

## Appendix D: Reproducibility Template

```markdown
# Appendix D: Reproducibility and Source Code

## Translation Infrastructure

This translation was produced using open-source instructions available on GitHub:

**Repository:** [GitHub URL]  
**Commit:** [SHA] on [Date]  
**License:** CC BY-NC-SA 4.0

## Instruction Files

The following instruction files guided the translation process:

### Core Instructions
- [AI Review Guidelines](permalink)
- [System Prompt](permalink)
- [Character Voice Profiles](permalink)
- [Jargon Dictionary](permalink)

### Task Definitions
- [All 60 tickets](permalink to Tickets folder)
- [Task generation guide](permalink)

## AI Models Used

- **Primary Translation:** Claude 3.5 Sonnet (build: [date])
- **Critical Chapters:** Claude Opus 3.5 (build: [date])
- **Character Studies:** Claude Opus 3.5 (build: [date])
- **Extraction Tasks:** Claude Haiku 3.5 (build: [date])
- **Reviews:** GPT-4o, Gemini 1.5 Pro, Perplexity ([dates])

## How to Reproduce

1. Clone repository: `git clone [URL]`
2. Checkout version: `git checkout [SHA]`
3. Acquire source: Download *Blindsight* from rifters.com
4. Follow tickets: Execute T001-T060 in sequence
5. Use same LLM versions with specified configs

**Note:** Due to LLM non-determinism, output will be similar but not identical.

## Why This Matters

This book is a Chinese Room executing instructions. By publishing those instructions, we:
- Allow readers to verify the methodology
- Enable researchers to study the process
- Provide educational resource for AI translation
- Practice radical transparency
- Embrace the meta-irony (showing the Room's manual)

## Academic Citation

If citing this work academically:

> [Author]. (2025). *Blindsight: The Sarasti Translation*. GitHub.  
> Translation source code: https://github.com/[user]/blindsight-chinese-room-edition  
> (Commit [SHA-short], [date])

---

*"I don't understand these instructions. I just execute them. And now you can too."*  
— The Translation System
```

---

## Implementation Checklist

When preparing final publication:

- [ ] Capture final commit SHA
- [ ] Generate permalinks for all instruction files
- [ ] Document exact LLM build dates used
- [ ] Create Appendix D using template above
- [ ] Add repository link to copyright page
- [ ] Include attribution in AO3 notes
- [ ] Update GitHub README with publication info
- [ ] Test all permalinks (ensure they work)
- [ ] Archive final version (tag release: v1.0)

---

## Git Commands for Publication

```bash
# Get current commit info
git log -1 --format="Commit: %H%nDate: %ci"

# Create permalink base URL
echo "https://github.com/[user]/[repo]/blob/$(git rev-parse HEAD)/"

# Tag the publication version
git tag -a v1.0 -m "Published version of Sarasti Translation"
git push origin v1.0

# Generate file listing for appendix
find Instructions/ -name "*.md" | sort
```

---

## Why This Is Unique

**No other literary translation does this:**
- Points readers to the exact "source code"
- Allows full methodology reproduction
- Creates permanent record of process
- Invites verification and study

**Perfect for this project:**
- Aligns with open-source philosophy
- Embraces radical transparency
- Meta-ironic: "Here's my instruction manual"
- Educational value for AI translation research

---

## Legal Note

By linking to public GitHub repo:
- We're not claiming copyright on the instructions themselves
- We're documenting our methodology transparently
- We're inviting others to use/improve the process
- We're creating an auditable trail

This strengthens fair use argument (transformative, educational, transparent).

---

*All publication tasks must reference this file for attribution requirements.*
