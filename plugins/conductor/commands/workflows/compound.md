---
name: compound
description: Self-improvement - collect suggestions, propose updates to docs/templates/agents
argument-hint: "[optional focus area]"
---

# Compound Command

Make the system better over time by collecting and surfacing improvement opportunities.

## Input

<focus_area> #$ARGUMENTS </focus_area>

If no focus area is provided, review all sources of improvement suggestions.

## Workflow

### 1. Gather suggestions

Look for improvement opportunities from:
- Agent mail / notes (once that skill exists)
- Patterns from recent `/plan`, `/work`, `/review` sessions
- Friction points or repeated manual steps
- Feedback Dan has given

<!-- TODO: Define where agent mail / notes live -->
<!-- TODO: Define how to detect patterns across sessions -->

### 2. Categorize and prioritize

Group suggestions by type:
- **Agents:** New agents to add, or improvements to existing ones
- **Commands:** Workflow changes, new commands
- **Skills:** New reusable capabilities
- **Docs:** Updates to CLAUDE.md, templates, style guides
- **Other:** Anything that doesn't fit above

Prioritize by:
- Frequency (how often does this come up?)
- Impact (how much time/friction would it save?)
- Effort (how hard is it to implement?)

### 3. Propose changes

For each high-priority suggestion, produce:
- **What:** Clear description of the change
- **Why:** What problem it solves
- **How:** Rough implementation approach

**Important:** This command only **proposes** changes. Dan decides what to implement.

### 4. Output

Write proposals to `compound/proposals/<date>-<slug>.md`

Present a summary:
- X new proposals generated
- Top 3 by impact
- Any that should be discussed immediately

---

## Principles

- **Self-improving:** The system should get better with use
- **Human decides:** Proposals, not automatic changes
- **Compounding:** Small improvements add up over time

---

## Future enhancements

<!-- TODO: Define agent-mail skill for inter-agent communication -->
<!-- TODO: Add pattern detection across sessions -->
<!-- TODO: Consider periodic "compound review" reminders -->

