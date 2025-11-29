---
name: work
description: Execute a plan in small steps, producing stacked PRs with succinct descriptions
argument-hint: "[plan file or todo file]"
---

# Work Command

Take a plan and execute it systematically, producing clean PRs ready for review.

## Input

<plan_file> #$ARGUMENTS </plan_file>

If no file is provided, ask: "Which plan should I work on?" and list available plans in `plans/`.

## Workflow

### Phase 1: Understand the plan

- Read the plan file completely
- Identify any ambiguities and ask clarifying questions **now**, not mid-implementation
- Get explicit approval before starting work

<!-- TODO: Define what "understanding" looks like - checklist? summary? -->

### Phase 2: Break down into tasks

- Create a todo list from the plan
- Order tasks by dependency
- Keep tasks small enough to complete and verify individually

<!-- TODO: Wire to a file-based todo skill once defined -->

### Phase 3: Implement tasks

For each task:
1. Mark as in-progress
2. Implement the change
3. Verify it works (run tests, manual check, etc.)
4. Mark as complete
5. Commit with a clear message

<!-- TODO: Define test commands per project type -->
<!-- TODO: Define commit message format -->

### Phase 4: PR prep

When a logical chunk is complete:
- Create a PR with a succinct description
- Call out what the reviewer should pay attention to
- Link to the plan/issue if applicable

<!-- TODO: Define PR template -->
<!-- TODO: Consider stacked PR workflow -->

---

## Principles

- **Finish what you start:** Don't leave tasks 80% done
- **Small commits:** Easier to review, easier to revert
- **Clear PRs:** The reviewer's time is valuable

---

## Future enhancements

<!-- TODO: Wire to workflow agents once defined -->
<!-- TODO: Add support for stacked PRs -->
<!-- TODO: Integrate with todo/triage skill -->

