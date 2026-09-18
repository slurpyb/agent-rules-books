---
name: the-pragmatic-programmer
description: Apply Hunt and Thomas-inspired pragmatic programming rules when improving engineering judgment, feedback loops, DRY knowledge, orthogonality, automation, prototyping, or adaptable design.
license: MIT
---

# The Pragmatic Programmer Skill

Use this skill when a task involves pragmatic engineering judgment, responsibility, DRY at the knowledge level, orthogonality, automation, prototyping, fast feedback, or adaptable design.

## Instructions

1. Read and apply [the-pragmatic-programmer.mini.md](../../the-pragmatic-programmer.mini.md) before making design or code decisions.
2. Use [the-pragmatic-programmer.md](../../the-pragmatic-programmer.md) only as deeper reference when the mini rules are not enough for the current tradeoff.
3. Prefer outcome-driven judgment over ceremony: reduce duplicated knowledge, keep concerns independent, shorten feedback loops, and leave the system easier to change.
4. When reviewing or auditing a change for pragmatic fitness, delegate to the `pragmatic-reviewer` subagent so the checklist runs in an isolated context.

## Companion plugin pieces

- Granular Cursor rules: [../../rules/](../../rules/) (Apply Intelligently by topic)
- Review subagent: [../../agents/pragmatic-reviewer.md](../../agents/pragmatic-reviewer.md)
