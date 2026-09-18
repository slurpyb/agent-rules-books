# Refactoring (Cursor Plugin)

Martin Fowler-inspired guidance as a Cursor plugin: skill, granular rules, and a review subagent.

## Components

| Component | Path | Role |
| --- | --- | --- |
| Skill | [`skills/refactoring/`](skills/refactoring/) | On-demand workflow guidance (`mini`, with `full` as reference) |
| Rules | [`rules/`](rules/) | Apply Intelligently `.mdc` topic rules split from the full source |
| Agent | [`agents/refactoring-reviewer.md`](agents/refactoring-reviewer.md) | Read-only subagent for audits in an isolated context |
| Canonical sources | `refactoring.md` / `refactoring.mini.md` / `refactoring.nano.md` | Tool-agnostic rule sets |
| Skills CLI entry | [`SKILL.md`](SKILL.md) | Root entry for `npx skills` and other Agent Skills clients |

## When to use which

- **Skill**: active implementation or design work that should follow Refactoring defaults.
- **Rules**: ordinary coding where Cursor should attach only the relevant topic.
- **`refactoring-reviewer` subagent**: PR review, post-change audit, or independent verification without flooding the main chat.

## Install

This directory is listed in the repo marketplace as the `refactoring` plugin (see [`.cursor-plugin/marketplace.json`](../.cursor-plugin/marketplace.json)).

For Agent Skills CLI:

```sh
npx skills add ciembor/agent-rules-books --skill refactoring
```
