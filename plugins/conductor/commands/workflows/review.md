---
name: review
description: Surface high-signal questions and overbuild/underbuild risks for code review
argument-hint: "[PR number, URL, or branch]"
---

# Review Command

Perform a code review that surfaces the things Dan would actually care about.

## Input

<review_target> #$ARGUMENTS </review_target>

If no target is provided:
- Check if on a feature branch with an open PR → use that
- Otherwise, ask: "Which PR or branch should I review?"

## Review perspectives

Focus on what matters, skip the noise.

### 1. Taste check

- Does this meet the quality bar?
- Is there "AI slop" - generic, over-engineered, or soulless code?
- Would I be proud to ship this?

### 2. Overbuild / underbuild

- Is this more complex than it needs to be?
- Is it too simple and missing important cases?
- Did we build the right thing?

### 3. Subtle bugs

- Race conditions, edge cases, error handling
- Things that are easy to miss in a quick scan
- Issues that would only surface in production

### 4. Human-in-the-loop moments

- What decisions need Dan's input?
- What tradeoffs were made that should be validated?
- What's the reviewer's confidence level?

---

## Output

Present findings in priority order:
1. **Blockers:** Must fix before merge
2. **Concerns:** Should discuss or fix
3. **Suggestions:** Nice to have

For each finding:
- What's the issue?
- Where is it? (file + line)
- What's the suggested fix or question?

---

## Future multi-agent orchestration

<!-- TODO: Define reviewer agents that encode specific review criteria -->
<!-- TODO: Add Task reviewer-name(...) calls here once agents exist -->
<!-- TODO: Consider parallel vs sequential review passes -->

---

## Principles

- **High signal:** Don't waste time on nitpicks
- **Human-in-the-loop:** Surface questions, don't just approve/reject
- **Actionable:** Every finding should have a clear next step

