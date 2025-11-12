# T062: Literary Style Analysis

**Stage:** 1-Research  
**Status:** TODO  
**LLM:** Claude Opus 4.1  
**Estimated Cost:** $15-20  
**Estimated Time:** 8-12 hours  
**Depends On:** T002 (Markdown conversion complete)

---

## Context Requirements

**Documents to Read BEFORE Starting:**

**MANDATORY:**
- [ ] `Instructions/Literary-Style-Analysis-Template.md` - The template you will fill out
- [ ] All 22 chapters from T002 output (complete novel in Markdown)
- [ ] `Documentation/Character-Philosophy.md` - Understanding character voice importance

**Supporting:**
- [ ] `Documentation/Audience-Analysis.md` - Why style matters for bounced readers
- [ ] `Documentation/Technical-Approach.md` - Quality standards and philosophy

**Critical:** This is a deep, technical analysis. You must read the entire novel with the template open, filling in each section systematically. This will take many hours. Do not rush.

---

## Objective

Analyze Peter Watts' *Blindsight* to create a comprehensive literary style guide documenting all prose techniques, narrative patterns, and stylistic choices. This guide becomes the technical manual for replicating Watts' voice in translation.

---

## Process

### Phase 1: First Complete Read (3-4 hours)

1. **Read Novel With Template Open**
   - Read all 22 chapters sequentially
   - Have `Literary-Style-Analysis-Template.md` open alongside
   - Take notes on initial impressions
   - Mark passages that exemplify each template section
   - Don't try to complete template yet—just observe

2. **Identify Major Patterns**
   - What makes Watts' prose distinctive?
   - What techniques appear repeatedly?
   - What would be hardest to replicate?
   - What must be preserved vs. can be adapted?

### Phase 2: Systematic Analysis (4-6 hours)

3. **Work Through Template Section by Section**
   
   **For each of the 12 template sections:**
   
   a. **Re-read relevant passages**
      - Find 5-10 examples of this element
      - Note chapter and approximate location
      - Copy exact quotes for reference
   
   b. **Identify patterns**
      - What's the typical usage?
      - What are the variations?
      - What are the rules (explicit or implicit)?
      - What are the exceptions?
   
   c. **Fill in checkboxes with detail**
      - Not just "yes" but "here's how and why"
      - Provide 3-5 specific examples per checkbox
      - Include chapter references
      - Explain the technique's effect
   
   d. **Note translation implications**
      - What must be preserved exactly?
      - What can be adapted for clarity?
      - What risks exist in changing this?

4. **Focus Areas (spend extra time on these):**
   
   **Narrative Voice (Section 1):**
   - Keeton's synthesist perspective is CORE
   - His clinical detachment shapes everything
   - How does unreliable narration work?
   - Examples of affect-less description
   
   **Technical Language (Section 3):**
   - Jargon integration is key challenge for bounced readers
   - How does Watts make dense science readable?
   - When does he explain vs. assume understanding?
   - Examples of elegant exposition
   
   **Dialogue (Section 4):**
   - Each character has distinct voice
   - Sarasti especially must be captured
   - How much is said vs. implied?
   - Examples of subtext and voice
   
   **Kayfabe & Meta-Narrative (Section 8):**
   - Critical for our translation frame
   - How does Watts maintain fictional reality?
   - Self-aware moments vs. immersion
   - Examples of meta-commentary

### Phase 3: Synthesis & Refinement (1-2 hours)

5. **Review Completed Template**
   - Have you filled in every checkbox?
   - Are examples specific and actionable?
   - Are patterns clearly described?
   - Are rules replicable?

6. **Add Cross-References**
   - Link related sections (dialogue voice + character philosophy)
   - Note how elements interact (rhythm affects tone)
   - Identify dependencies (POV shapes everything)

7. **Write Introduction Section**
   - Overview of Watts' style in 2-3 paragraphs
   - Key principles for translators
   - How to use this guide
   - What matters most vs. details

8. **Write Translation Guidelines Section**
   - Top 10 rules for maintaining Watts' voice
   - What to preserve at all costs
   - What can be adapted for clarity
   - Common pitfalls to avoid

### Phase 4: Validation (30 minutes)

9. **Self-Test**
   - Pick a random chapter section (not previously analyzed)
   - Try to describe its style using only your completed template
   - Does your analysis predict the actual prose?
   - If not, refine template until it does

10. **Quality Check**
    - [ ] Every template section is filled in
    - [ ] 3-5 examples per element
    - [ ] Chapter references provided
    - [ ] Patterns are clearly described
    - [ ] Rules are actionable
    - [ ] Translation implications noted
    - [ ] Could someone replicate Watts' style using this guide?

---

## Inputs Required

- [ ] `Instructions/Literary-Style-Analysis-Template.md` - Empty template to fill
- [ ] All 22 chapters in Markdown (T002 output)
- [ ] `Documentation/Character-Philosophy.md` - Voice importance context
- [ ] `Documentation/Audience-Analysis.md` - Why style matters

---

## Outputs

```
Tasks/01-Research/Literary-Style-Guide.md
```

**Expected Format:** Completed template with all sections filled  
**Expected Length:** 15,000-25,000 words (30-50 pages)  
**Expected Depth:** Specific enough that an LLM could replicate Watts' style without reading the novel  

---

## Success Criteria

- [ ] All 12 template sections completely filled
- [ ] Every checkbox has detailed analysis (not just yes/no)
- [ ] 3-5 specific examples per element with chapter references
- [ ] Patterns are described, not just individual instances
- [ ] Rules are actionable and replicable
- [ ] Translation implications are explicit
- [ ] Introduction and guidelines sections added
- [ ] Cross-references between related elements
- [ ] Self-test validation passed
- [ ] Document is 15,000+ words (thorough, not superficial)

---

## Quality Standards

**Depth Over Breadth:**
- Better to deeply analyze one element than superficially list many
- Each example should include: quote, chapter reference, technique used, why it works, translation note
- Don't just describe what Watts does—explain HOW to replicate it

**Actionable Rules:**
- Not: "Watts uses short sentences for tension"
- But: "In action scenes, 60% of sentences are <10 words, with frequent fragments starting with verbs. Example: Chapter 4, Scrambler attack—'Alarms. Screaming metal. The ship lurched sideways.' Effect: creates urgency. Translation: preserve sentence breaks even if combining would be clearer."

**Translation Focus:**
- This isn't literary criticism—it's a technical manual
- Every observation should help translators make decisions
- Note what must be preserved vs. what can adapt
- Identify risks in changing each element

**Completeness:**
- If a section seems not applicable, explain why
- If Watts doesn't use a technique, note that explicitly
- Don't skip checkboxes—address each one
- Empty sections are failure; brief but complete is success

---

## Common Pitfalls to Avoid

**Don't:**
- Summarize plot or themes (that's in other tasks)
- Offer literary criticism or personal opinions
- Skip examples or use vague descriptions
- Rush through sections to "finish"
- Assume translators know what you mean

**Do:**
- Provide specific, quotable examples
- Explain why techniques work (effect on reader)
- Note chapter/page references for everything
- Take time to find representative patterns
- Think like a technical writer, not a book reviewer

---

## Notes

- **This is one of the most important research tasks.** The style guide will be used for all 22 chapter translations.
- **Estimated time is 8-12 hours.** This is correct. You're reading a dense novel and creating a technical manual.
- **Opus 4.1 is assigned** because this requires deep literary analysis and pattern recognition.
- **The completed guide becomes mandatory reading** for T018-T040 (all translation tasks) and T061 (preface generation).
- **If translation voice feels wrong, the problem is likely here.** A thorough style analysis prevents voice drift.

---

## Example Analysis (For Inspiration)

**Bad Analysis (too vague):**
> Watts uses metaphors. Example: "like a Chinese Room." This shows his themes.

**Good Analysis (actionable):**
> **Metaphor: Chinese Room Motif**  
> Usage: Appears 7 times in novel (Ch 1, 4, 8, 12, 15, 19, 22).  
> Pattern: Never explained directly—assumes reader knows Searle's thought experiment. First mention (Ch 1, p.12): "I was a Chinese Room running on crude heuristics." Context: Keeton describing post-surgery consciousness. Effect: Establishes philosophical frame immediately, rewards educated readers, creates density for others.  
> Translation Note: PRESERVE exact phrase "Chinese Room"—it's load-bearing for entire project's meta-irony. Consider adding subtle context in translation preface but not in text itself. Risk: If you explain it inline, you break Watts' show-don't-tell philosophy.

**This level of detail is the standard.**

---

## Completion Statement

When finished, add this to the top of your completed guide:

> **Literary Style Guide: Complete**  
> Analyzed by: [LLM name and version]  
> Date: [Date]  
> Total Examples: [Count]  
> Word Count: [Count]  
> Ready for use in: T018-T040 (Translation), T061 (Preface)

Then mark T062 as DONE.
