# T003: Keeton Character Study

**Stage:** 1-Research  
**Status:** TODO  
**LLM:** Claude Opus 3.5  
**Estimated Cost:** $3  
**Estimated Time:** 2-3 hours  
**Depends On:** T002

---

## Objective

Generate a comprehensive character analysis of Siri Keeton (POV narrator) including personality traits, speech patterns, character arc, and every significant quote.

---

## Process

### 1. Data Collection
- Read all 22 chapters focusing on Keeton's narration
- Extract all first-person observations
- Note internal monologue patterns
- Identify key character moments

### 2. LLM Analysis Prompt

```markdown
You are analyzing Siri Keeton, the narrator of Peter Watts' Blindsight.

TASK: Create a comprehensive character study (1500+ lines) covering:

1. ROLE & BACKGROUND
   - Synthesist (translator between specialists)
   - Neurologically modified (half brain removed in childhood)
   - Struggling with emotion/empathy

2. PERSONALITY TRAITS
   - Self-doubt and uncertainty
   - Clinical detachment
   - Intellectual curiosity
   - Learning to "feel"

3. SPEECH PATTERN ANALYSIS
   Extract examples of:
   - Technical jargon usage
   - Metaphors and descriptions
   - Internal dialogue style
   - Emotional language (or lack thereof)

4. CHARACTER ARC
   - Beginning state
   - Key turning points
   - End state
   - Growth/change

5. KEY RELATIONSHIPS
   - With Sarasti (fear/fascination)
   - With Chelsea (lost love)
   - With crew members

6. CRITICAL SCENES
   List 10+ pivotal moments with chapter references

7. VOICE TRANSLATION RULES
   Create patterns for converting his technical narration to accessible prose:
   - ORIGINAL: "The synaptic topology suggested..."
   - TRANSLATE TO: "Something in the way his neurons fired..."

OUTPUT: Markdown file with extensive quotes, analysis, and translation guidelines.
```

### 3. Human Review
- Verify accuracy of extracted quotes
- Check character arc interpretation
- Validate translation rules make sense

---

## Outputs

```
Tasks/01-Research/character-studies/keeton-deep-dive.md
```

**Expected Length:** 1500+ lines  
**Structure:**
- Role & Background (100 lines)
- Personality Traits (200 lines)
- Speech Patterns (300 lines)
- Character Arc (200 lines)
- Relationships (200 lines)
- Critical Scenes (300 lines)
- Translation Rules (200 lines)

---

## Quality Gates

- [ ] 1500+ lines of analysis
- [ ] 50+ direct quotes from text
- [ ] Complete character arc documented
- [ ] Translation rules created (technical→accessible)
- [ ] All key scenes identified with chapter refs
- [ ] LLM analysis validated by human

---

## LLM Configuration

**Model:** Claude Opus 3.5  
**Why:** Best at nuanced character analysis, worth premium cost for foundation  
**Context:** Feed all 22 chapters (full novel context)  
**Temperature:** 0.3 (analytical, not creative)

---

## Success Criteria

This character study will be referenced by every chapter translation. It must be:
- **Comprehensive:** Cover all aspects of character
- **Accurate:** Quotes verified, arc correct
- **Actionable:** Translation rules clear and usable

---

## Notes

- Keeton is the POV character - this is the MOST important character study
- His voice sets the tone for the entire translation
- Take time to get this right - it's foundational

---

**Previous Task:** T002 (Convert to Markdown)  
**Next Tasks:** 
- T004 (Sarasti Character Study)
- T008 (Extract Keeton Dialogue)
