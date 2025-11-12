# T002: Convert to Markdown (22 Chapters)

**Stage:** 1-Research  
**Status:** TODO  
**LLM:** N/A (Script/Human)  
**Estimated Cost:** $0  
**Estimated Time:** 1-2 hours  
**Depends On:** T001

---

## Objective

Convert the source *Blindsight* text into clean Markdown format, one file per chapter (22 total).

---

## Process

1. **Identify Chapter Breaks**
   - Read through source to find chapter divisions
   - *Blindsight* has ~22 chapters (verify exact count)
   - Note chapter titles/numbers

2. **Conversion Methods**

   **Option A: Manual Split (Recommended for Quality)**
   - Copy/paste each chapter into separate .md file
   - Clean formatting as you go
   - Preserve chapter structure

   **Option B: Automated Script**
   - Use Pandoc: `pandoc blindsight.html -o blindsight.md`
   - Then split by chapter markers with script
   - More error-prone, requires validation

3. **Formatting Standards**
   - Chapter file naming: `chapter-01-original.md`, `chapter-02-original.md`, etc.
   - Remove page numbers, headers, footers
   - Preserve paragraph breaks
   - Keep scene break markers (*** or similar)
   - No extra whitespace

4. **Validation**
   - Word count check (ensure nothing missing)
   - Read first/last paragraph of each chapter (continuity)
   - Check for conversion artifacts (weird characters, broken formatting)

---

## Outputs

```
Tasks/01-Research/source-material/
├── chapter-01-original.md
├── chapter-02-original.md
├── chapter-03-original.md
└── ... (through chapter-22-original.md)
```

---

## Quality Gates

- [ ] All 22 chapters extracted
- [ ] Clean Markdown formatting (no HTML artifacts)
- [ ] Chapter breaks preserved correctly
- [ ] Total word count matches original (~100K words)
- [ ] No missing paragraphs or sections
- [ ] Consistent naming convention

---

## Tools

- **Pandoc** (for initial conversion)
- **Text editor** (VS Code, Obsidian, etc.)
- **Word count tool** (verify completeness)

---

## Notes

- This is foundational - quality here affects all downstream work
- Take time to get formatting right (saves headaches later)
- Create a metadata file noting source, date, word count

---

**Previous Task:** T001 (Acquire Source)  
**Next Task:** T003 (Keeton Character Study)
