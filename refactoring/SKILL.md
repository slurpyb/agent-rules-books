---
name: refactoring
description: Apply Martin Fowler-inspired refactoring rules when improving existing code structure while preserving observable behavior, detecting smells, or separating refactoring from feature work.
license: MIT
---

# Refactoring Skill

Use this skill when a task matches the description above.

Before making design or code decisions, read and apply [refactoring.mini.md](refactoring.mini.md). Use [refactoring.md](refactoring.md) only as a deeper reference when the mini rules are not enough for the current tradeoff.

## Cursor plugin

This book directory is also a Cursor plugin (see [README.md](README.md)):

- Plugin skill: [skills/refactoring/SKILL.md](skills/refactoring/SKILL.md)
- Apply Intelligently rules: [rules/](rules/)
- Review subagent: [agents/refactoring-reviewer.md](agents/refactoring-reviewer.md)

Prefer the plugin skill and rules inside Cursor. Use the `refactoring-reviewer` subagent for isolated audits.
