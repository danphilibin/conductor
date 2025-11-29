# Conductor

A personal delegation system that lets you operate more like a tech lead orchestrating a small team—setting direction, reviewing work, making key decisions—while offloading the grunt work of planning and building.

## Core values

- **No AI slop:** Output must meet your quality bar
- **Human-in-the-loop:** You review, decide, and course-correct—not disappear
- **Self-improving:** The system learns and adapts to your taste over time
- **Fast feedback loops:** Know quickly if something's working or needs intervention

## Installation

Add the plugin to Claude Code:

```bash
/plugin add /path/to/conductor/plugins/conductor
```

Or if publishing to a marketplace:

```bash
/plugin install conductor
```

## Commands

| Command | Description |
|---------|-------------|
| `/conductor:plan` | Turn a seed idea into a PRD in your preferred format |
| `/conductor:work` | Execute a plan in small steps, producing clean PRs |
| `/conductor:review` | Surface high-signal questions and risks for code review |
| `/conductor:compound` | Self-improvement—collect and propose system updates |

## Status

This is an early scaffold. Many pieces are intentionally stubbed and will evolve through use.

- Commands exist but have minimal behavior
- Agents, skills, and MCP servers are not yet defined
- The system will grow as patterns emerge from real usage

## Project structure

```
plugins/conductor/
├── .claude-plugin/
│   └── plugin.json       # Plugin manifest
├── agents/               # Specialized agents (stubbed)
│   ├── review/
│   ├── workflow/
│   ├── docs/
│   └── research/
├── commands/
│   ├── workflows/        # Core commands (plan, work, review, compound)
│   └── utility/          # Helper commands (future)
├── skills/               # Reusable capabilities (future)
├── CLAUDE.md             # Plugin guidance
└── CHANGELOG.md          # Version history
```

## Philosophy

Each unit of work should make subsequent work easier—not harder. This system is designed to compound your effectiveness over time by:

1. Codifying your preferences and patterns
2. Surfacing the right questions at the right time
3. Keeping you in the loop without drowning in details
4. Learning from feedback and improving itself

