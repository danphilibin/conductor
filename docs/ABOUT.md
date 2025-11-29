# Conductor

_Personal delegation system for orchestrating AI agents_

## Mission

Build a delegation system that lets me operate more like a tech lead orchestrating a small team - setting direction, reviewing work, making key decisions - while offloading the grunt work of planning and building, so I can apply my judgment and taste to more things without drowning in execution details or producing garbage code.

## Core Values & Constraints

- **No AI slop**: The output has to meet my quality bar - this is non-negotiable because my whole value prop is taste
- **Keeps me in the loop**: I'm not trying to disappear - I still want to review, make decisions, course-correct. Just not write every line or plan every detail
- **Increases surface area**: The point is I can work on more things simultaneously (Relay + side project + Corner) without feeling scattered or like I'm making linear progress
- **Fast feedback loops**: If delegating to an agent takes 30 minutes to plan, it's not worth it. I need to know quickly if something's working or needs my intervention. Focus on finding friction points and reducing them.
- **Self-improving**: The system should learn and adapt to my personal taste over time - my specific preferences for code style, architecture decisions, what constitutes "done", etc. This becomes part of my highly customized personal toolkit.

## System Shape

A Claude Code plugin with commands + sub-agents, similar to Compounding Engineering but built for my own tastes.

## Commands

### /plan

Take a kernel of an idea (with as much or as little detail as I feel is necessary) and flesh it out into a PRD in a format that makes sense to me.

**Current pain points with existing tools:**

- Docs are too long, too much to read
- Not broken effectively into small tasks
- Not easily editable depending on which tool I'm using

**Features:**

- T-shirt sizing (SM project has different format than XL project)
- Standard formatting
- End goal: I love love love using this tool to plan without any of the friction I feel with other tools

### /work

Designed to take the output of a planning session and work on individual pieces.

**Features:**

- Issue tracking + operationalizing the workflow of "take piece of work, do it, and open a PR for review"
- PRs are succinct, well-written, and call out what I should pay attention to
- Designed really well for sequential work (think: stacked PRs?)
- Addresses shortcoming: many tools struggle with sequential work

### /review

Explore how I could delegate code review to AI.

**Key insight:** If I use AI to plan, another agent to work, and feed the output into a code review agent - what might it look like if the review agent says "whoa, you really over-built this - dan, did he overbuild it?"

**Inspiration:**

- OpenAI Codex code reviews at work are SUPER effective at calling out really subtle bugs I would otherwise miss
- Gut-check stuff that helps surface high-signal issues

**Note:** The human has to be in the loop SOMEWHERE - this is about surfacing the right questions/concerns, not replacing judgment

### /compound

The self-improvement component - make this a self-improving system.

**Possible features:**

- Recommending new agents to add
- Updates to docs, style guides, templates, etc.
- "Agent mail" system where agents write notes to each other in a file
- System keeps track of notes and has tools for incorporating suggested improvements
- /compound reads the mail + captures what to improve

**Status:** Most open-ended - research project to figure out the best format

## Next Steps

Start ridiculously small. Pick one annoying repeated task and build something that handles just that one thing in a way that actually matches how I think. Don't try to build the whole system yet.

Timebox exploration to ~1 hour every Saturday morning, see what emerges.

## Meta Notes

This is an experiment to see if I can work this way. Might discover it feels terrible or that the overhead is worse than doing it myself. Or might discover I'm actually pretty good at it and it unlocks a new gear.

Building this skill also helps prepare for senior roles where I'll need to be comfortable reviewing code and guiding work rather than always being hands-on-keyboard.
