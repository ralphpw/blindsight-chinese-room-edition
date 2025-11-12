# TODO: Deferred Tasks

**Purpose:** Track infrastructure and implementation tasks deferred for later completion.

**Status:** Living document - update as items are completed or new ones identified  
**Last Updated:** 2025-11-12

---

## MCP Server Development

### Priority: HIGH
### Estimated Time: 4-6 hours

**Tasks:**
- [ ] Create MCP server project structure (TypeScript/Node.js)
- [ ] Implement core tools:
  - [ ] `execute_ticket` - Run single ticket in fresh API session
  - [ ] `execute_stage` - Loop through stage tickets
  - [ ] `update_kanban` - Write progress back to KANBAN.md
  - [ ] `generate_failure_report` - Create error reports on abort
- [ ] Add KANBAN parser (read ticket metadata from table)
- [ ] Add ticket file parser (read context requirements)
- [ ] Implement context file loader with token counting
- [ ] Add summarization detection prompt injection
- [ ] Implement LLM client factory (Anthropic, OpenAI, etc.)
- [ ] Add KANBAN writeback functionality
- [ ] Configure API keys in MCP settings
- [ ] Test with single ticket (T062 or T063)
- [ ] Document MCP server usage in README

**Dependencies:**
- Anthropic API key
- OpenAI API key (optional, for GPT-4o reviews)
- MCP SDK installation
- Token counting library (tiktoken or similar)

---

## MCP Server Testing

### Priority: HIGH
### Estimated Time: 2-3 hours

**Test Cases:**
- [ ] **Token budget validation:** Reject ticket if context exceeds 50% limit
- [ ] **Summarization detection:** Abort if LLM returns "ABORT:" signal
- [ ] **Fresh session isolation:** Verify new client created per ticket
- [ ] **KANBAN writeback:** Confirm status updates persist to file
- [ ] **Context loading:** Verify only specified files loaded
- [ ] **LLM selection:** Test switching between Opus/Sonnet/GPT-4o
- [ ] **Failure recovery:** Generate report on error, ask to continue
- [ ] **Stage execution:** Run multiple tickets in sequence
- [ ] **Mid-stage restart:** Mark some tickets DONE, resume from next

**Test Tickets:**
- T062 (Literary Style Analysis) - 120K tokens, Opus
- T063 (Voice Consolidation) - 30K tokens, Haiku
- T001-T003 (Source reading) - Various token levels

---

## Ticket Generation

### Priority: MEDIUM
### Estimated Time: 3-4 hours

**Remaining Tickets to Generate:**
- [ ] T004-T012 (Stage 1: Research - 9 tickets)
- [ ] T014-T017 (Stage 1: Research - 4 tickets)
- [ ] T019-T039 (Stage 3: Chapters 2-22 - 21 tickets)
- [ ] T042-T046, T048 (Stage 4: Reviews - 6 tickets)
- [ ] T049, T051-T060 (Stage 5: Publication - 11 tickets)

**Total:** ~51 tickets to generate

**Template:** Use `Instructions/TEMPLATE.md` and `TICKET-GENERATION-GUIDE.md`

**Pattern:**
1. Copy TEMPLATE.md
2. Fill in context requirements (consult Context-Window-Management.md)
3. Add token budget calculation
4. Define success criteria
5. Save to `Instructions/Tickets/`

---

## Context Requirements Population

### Priority: MEDIUM
### Estimated Time: 1-2 hours

**Tickets needing context requirements review:**
- [x] T018 (Chapter 1) - Already has context requirements
- [ ] T041 (Internal Consistency Review)
- [ ] T047 (Grok Backstop)
- [ ] T050 (Attribution Philosophy)
- [ ] T061 (Generate Preface)
- [ ] T062 (Literary Style Analysis)
- [ ] T063 (Consolidate Character Voice Reference)

**Action:** Add/verify "Context Requirements" section in each ticket

---

## Token Budget Verification

### Priority: LOW
### Estimated Time: 1 hour

**Tasks:**
- [ ] Build token counting script (`scripts/count_tokens.py`)
- [ ] Verify each ticket's context fits within budget
- [ ] Update KANBAN with actual token measurements
- [ ] Flag any tickets exceeding 50% threshold

---

## Documentation Cleanup

### Priority: LOW
### Estimated Time: 30 minutes

**Tasks:**
- [ ] Review all Documentation/ files for consistency
- [ ] Ensure cross-references are correct
- [ ] Update dates to 2025-11-12
- [ ] Check for broken links

---

## Notes

**Blockers:** None currently  
**Next Action:** Implement MCP server core functionality
