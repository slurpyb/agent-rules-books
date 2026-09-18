# The Pragmatic Programmer (Cursor Plugin)

Hunt & Thomas-inspired pragmatic engineering as a Cursor plugin: skill, granular rules, and a review subagent.

## Components

| Component | Path | Role |
| --- | --- | --- |
| Skill | [`skills/the-pragmatic-programmer/`](skills/the-pragmatic-programmer/) | On-demand workflow guidance (`mini`, with `full` as reference) |
| Rules | [`rules/`](rules/) | 24 Apply Intelligently `.mdc` topic rules split from the full source |
| Agent | [`agents/pragmatic-reviewer.md`](agents/pragmatic-reviewer.md) | Read-only subagent for pragmatic audits in an isolated context |
| Canonical sources | `the-pragmatic-programmer.md` / `.mini.md` / `.nano.md` | Tool-agnostic rule sets |
| Skills CLI entry | [`SKILL.md`](SKILL.md) | Root entry for `npx skills` and other Agent Skills clients |

## When to use which

- **Skill**: active implementation or design work that should follow pragmatic defaults.
- **Rules**: ordinary coding where Cursor should attach only the relevant topic (DRY, automation, contracts, …).
- **`pragmatic-reviewer` subagent**: PR review, post-change audit, or independent verification without flooding the main chat with the full checklist.

## Install

This directory is listed in the repo marketplace as the `the-pragmatic-programmer` plugin (see [`.cursor-plugin/marketplace.json`](../.cursor-plugin/marketplace.json)).

For Agent Skills CLI:

```sh
npx skills add ciembor/agent-rules-books --skill the-pragmatic-programmer
```
