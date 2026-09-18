# Clean Code (Cursor Plugin)

Robert C. Martin-inspired guidance as a Cursor plugin: skill, granular rules, and a review subagent.

## Components

| Component | Path | Role |
| --- | --- | --- |
| Skill | [`skills/clean-code/`](skills/clean-code/) | On-demand workflow guidance (`mini`, with `full` as reference) |
| Rules | [`rules/`](rules/) | Apply Intelligently `.mdc` topic rules split from the full source |
| Agent | [`agents/clean-code-reviewer.md`](agents/clean-code-reviewer.md) | Read-only subagent for audits in an isolated context |
| Canonical sources | `clean-code.md` / `clean-code.mini.md` / `clean-code.nano.md` | Tool-agnostic rule sets |
| Skills CLI entry | [`SKILL.md`](SKILL.md) | Root entry for `npx skills` and other Agent Skills clients |

## When to use which

- **Skill**: active implementation or design work that should follow Clean Code defaults.
- **Rules**: ordinary coding where Cursor should attach only the relevant topic.
- **`clean-code-reviewer` subagent**: PR review, post-change audit, or independent verification without flooding the main chat.

## Install

This directory is listed in the repo marketplace as the `clean-code` plugin (see [`.cursor-plugin/marketplace.json`](../.cursor-plugin/marketplace.json)).

For Agent Skills CLI:

```sh
npx skills add ciembor/agent-rules-books --skill clean-code
```
