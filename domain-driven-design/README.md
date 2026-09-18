# Domain-Driven Design (Cursor Plugin)

Eric Evans-inspired guidance as a Cursor plugin: skill, granular rules, and a review subagent.

## Components

| Component | Path | Role |
| --- | --- | --- |
| Skill | [`skills/domain-driven-design/`](skills/domain-driven-design/) | On-demand workflow guidance (`mini`, with `full` as reference) |
| Rules | [`rules/`](rules/) | Apply Intelligently `.mdc` topic rules split from the full source |
| Agent | [`agents/ddd-reviewer.md`](agents/ddd-reviewer.md) | Read-only subagent for audits in an isolated context |
| Canonical sources | `domain-driven-design.md` / `domain-driven-design.mini.md` / `domain-driven-design.nano.md` | Tool-agnostic rule sets |
| Skills CLI entry | [`SKILL.md`](SKILL.md) | Root entry for `npx skills` and other Agent Skills clients |

## When to use which

- **Skill**: active implementation or design work that should follow Domain-Driven Design defaults.
- **Rules**: ordinary coding where Cursor should attach only the relevant topic.
- **`ddd-reviewer` subagent**: PR review, post-change audit, or independent verification without flooding the main chat.

## Install

This directory is listed in the repo marketplace as the `domain-driven-design` plugin (see [`.cursor-plugin/marketplace.json`](../.cursor-plugin/marketplace.json)).

For Agent Skills CLI:

```sh
npx skills add ciembor/agent-rules-books --skill domain-driven-design
```
