---
name: refactoring
description: Apply Martin Fowler-inspired refactoring rules when improving existing code structure while preserving observable behavior, detecting smells, or separating refactoring from feature work.
license: MIT
---

# Refactoring Skill

Use this skill when a task matches the description above.

## Instructions

1. Read and apply [refactoring.mini.md](../../refactoring.mini.md) before making design or code decisions.
2. Use [refactoring.md](../../refactoring.md) only as deeper reference when the mini rules are not enough for the current tradeoff.
3. When reviewing or auditing a change for Refactoring fitness, delegate to the `refactoring-reviewer` subagent so the checklist runs in an isolated context.

## Companion plugin pieces

- Granular Cursor rules: [../../rules/](../../rules/) (Apply Intelligently by topic)
- Review subagent: [../../agents/refactoring-reviewer.md](../../agents/refactoring-reviewer.md)
