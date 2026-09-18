# Refactoring — Cursor Rules

Granular Cursor project rules distilled from the full source in [`../refactoring.md`](../refactoring.md).

These `.mdc` files are packaged with the `refactoring` Cursor plugin (`rules/` is auto-discovered). Each rule uses **Apply Intelligently**: `alwaysApply: false` plus a specific `description` so the agent can load only the topics relevant to the current action.

## Rule index

| File | Load when |
| --- | --- |
| `change-checklist.mdc` | Apply as a final gate before finishing a refactoring: behavior preserved, steps small, smells reduced, tests green. |
| `primary-directive-and-scope.mdc` | Apply when deciding whether work is true refactoring, starting structural improvement, or separating behavior change from cleanup. |
| `non-negotiable-rules.mdc` | Apply when preserving behavior, working in small steps, keeping the system runnable, or doing preparatory refactoring before feature work. |
| `safety-rules.mdc` | Apply when establishing characterization tests, safety nets, commit discipline, or preparatory refactoring before risky structural change. |
| `code-smell-policy.mdc` | Apply when detecting or treating duplicated code, long functions, long parameter lists, divergent change, shotgun surgery, feature envy, data clumps, or related smells. |
| `preferred-refactoring-moves.mdc` | Apply when choosing extract, inline, rename, move, split, or simplify transformations during a refactoring pass. |
| `refactoring-catalog-index.mdc` | Apply when selecting a named Fowler refactoring technique for a specific smell or structural problem. |
| `function-level-rules.mdc` | Apply when extracting, simplifying, or reshaping functions during refactoring. |
| `class-and-module-rules.mdc` | Apply when moving responsibilities between classes or modules, splitting, or consolidating during refactoring. |
| `working-with-conditionals.mdc` | Apply Refactoring guidance on rules for working with conditionals when the current task involves rules for working with conditionals concerns. |
| `data-and-mutation-rules.mdc` | Apply when encapsulating fields, reducing mutable shared state, or replacing data clumps during refactoring. |
| `error-handling-rules.mdc` | Apply when restructuring error handling without changing observable failure behavior. |
| `review-rules.mdc` | Apply when reviewing a refactoring diff for behavior preservation, step size, and smell reduction. |
| `forbidden-patterns.mdc` | Apply when spotting rewrite-as-refactoring, mixed feature+cleanup patches, deleted tests, or unverified modernization. |
| `code-generation-rules.mdc` | Apply when generating or scaffolding refactored code that must preserve behavior and stay in small steps. |
| `testing-rules.mdc` | Apply when aligning tests with refactoring, characterization coverage, or verifying preserved behavior. |
| `stopping-rules.mdc` | Apply when deciding whether to stop refactoring, avoid gold-plating, or leave further cleanup for later. |

## Relationship to mini / nano / skill / subagent

- **Plugin skill** ([`../skills/refactoring/`](../skills/refactoring/)): loads `mini` by default for book-specific workflows.
- **Root skill entry** ([`../SKILL.md`](../SKILL.md)): Agent Skills CLI / portable entrypoint.
- **These rules**: split the **full** source for Cursor's intelligent, per-action attachment.
- **Subagent** ([`../agents/refactoring-reviewer.md`](../agents/refactoring-reviewer.md)): read-only audit in an isolated context.
- Prefer these over dumping the whole full file into an Always Apply rule. See [`../README.md`](../README.md).
