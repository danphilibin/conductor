---
name: plan
description: Turn a seed idea into a PRD in Dan's preferred format (S/M/L/XL sizing, scannable, no bloat)
argument-hint: "[idea or feature description]"
---

# Plan Command

Transform a rough idea into a structured PRD that's easy to scan and act on.

## Input

<idea> #$ARGUMENTS </idea>

If no idea is provided, ask: "What would you like to plan?"

## Output

A markdown PRD file in `plans/` with:
- Clear problem statement
- Acceptance criteria
- Task breakdown appropriate to project size

## Workflow

### 1. Clarify scope

Ask clarifying questions if the idea is ambiguous. Keep questions short and focused.

<!-- TODO: Define specific clarifying question patterns -->

### 2. Determine project size

Classify as S / M / L / XL based on estimated effort:
- **S (Small):** < 1 day, single PR
- **M (Medium):** 1-3 days, maybe 2-3 PRs
- **L (Large):** 1-2 weeks, multiple PRs
- **XL (Extra Large):** Multi-week, needs phased rollout

<!-- TODO: Define PRD template per size -->

### 3. Generate PRD

Create a PRD that is:
- **Scannable:** Headers, bullets, no walls of text
- **Actionable:** Clear next steps
- **Right-sized:** Detail proportional to project size

<!-- TODO: Define section structure and length constraints -->

### 4. Output location

Write to `plans/<slug>.md`

---

## Future enhancements

<!-- TODO: Wire to planning agents once defined -->
<!-- TODO: Add skill integration for research/context gathering -->
<!-- TODO: Define how to handle follow-up questions and iteration -->

