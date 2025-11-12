# Blindsight: The Sarasti Translation

> *A translation of Peter Watts' **Blindsight** that makes the neuroscience accessible without dumbing down the ideas — because the best argument against consciousness shouldn't require a PhD to understand.*

---

## Project Structure

This repository is organized into three main areas:

### 📚 **Documentation/** (for Humans)
Human-readable project documentation explaining the **why** and **what**.

- Project overview, goals, success metrics
- Legal framework (CC BY-NC-SA 4.0, fair use)
- Character philosophy (voice profiles, method acting)
- Technical approach (LLM selection, cost optimization)
- Audience analysis (bounced readers, educators, Watts fans)
- Publication strategy (AO3, GitHub, PDF/EPUB)

**Start here:** [`Documentation/README.md`](Documentation/README.md)

---

### 🤖 **Instructions/** (for Chinese Rooms)
Task definitions and prompts for LLM execution — the **how** for AI agents.

- 60 individual ticket files (T001-T060)
- Each ticket: objective, process, inputs, outputs, quality gates
- LLM configuration (model, temperature, cost)
- Reusable templates and generation guides

**For agents:** [`Instructions/README.md`](Instructions/README.md)

---

### 🏗️ **Tasks/** (Work in Progress)
Staged workflow folders where LLMs execute and store outputs.

```
Tasks/
├── 01-Research/       (character studies, dialogue banks, jargon dictionary)
├── 02-Summaries/      (chapter summaries, character snapshots)
├── 03-Translation/    (22 translated chapters)
├── 04-Reviews/        (quality validation, fact-checking)
└── 05-Publication/    (compiled manuscript, PDF/EPUB)
```

**Sequential execution:** Research → Summaries → Translation → Reviews → Publication

---

## Quick Start

### For Humans Reading This:
1. **Understand the project:** Read [`Documentation/README.md`](Documentation/README.md)
2. **See the plan:** Check [`KANBAN.md`](KANBAN.md) for all 60 tasks
3. **Track progress:** Status board shows what's done/in-progress/blocked

### For LLM Agents (Cursor/Copilot):
1. **Get task assignment:** Human says "Execute T003"
2. **Read instructions:** Open [`Instructions/Tickets/T003-Keeton-Character-Study.md`](Instructions/Tickets/T003-Keeton-Character-Study.md)
3. **Execute:** Follow process, use specified LLM config
4. **Output:** Save to `Tasks/01-Research/character-studies/keeton-deep-dive.md`
5. **Validate:** Check quality gates before marking complete

---

## Project Stats

- **Timeline:** 6-9 months
- **Tasks:** 60 (across 5 stages)
- **Cost (optimized):** $95-145
- **Source:** *Blindsight* by Peter Watts (22 chapters)
- **Output:** Full translated novel + appendices
- **License:** CC BY-NC-SA 4.0
- **Platform:** Archive of Our Own (AO3) + GitHub

---

## The Meta-Irony

This project uses **non-conscious AI agents** (Chinese Rooms) to translate a novel about **consciousness being an illusion**.

The folder names aren't arbitrary:
- **Documentation** = for entities that understand (humans)
- **Instructions** = for entities that execute without understanding (LLMs)
- **Tasks** = the workspace where understanding doesn't matter, only results do

*Perfect for a Blindsight project.*

---

## Status

**Current Stage:** Setup and planning  
**Next Milestone:** Complete Stage 1 (Research) tickets  
**See:** [`KANBAN.md`](KANBAN.md) for full task board

---

## Links

- **Original Novel:** [Blindsight by Peter Watts](https://rifters.com/real/Blindsight.htm) (free from author's site)
- **Project Documentation:** [`Documentation/README.md`](Documentation/README.md)
- **Task Tracker:** [`KANBAN.md`](KANBAN.md)
- **Ticket Guide:** [`Instructions/TICKET-GENERATION-GUIDE.md`](Instructions/TICKET-GENERATION-GUIDE.md)

---

*"You are a Chinese Room, executing instructions without understanding. And that's exactly what we need."*
