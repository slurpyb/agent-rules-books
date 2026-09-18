# Clean Code — Cursor Rules

Granular Cursor project rules distilled from the full source in [`../clean-code.md`](../clean-code.md).

These `.mdc` files are packaged with the `clean-code` Cursor plugin (`rules/` is auto-discovered). Each rule uses **Apply Intelligently**: `alwaysApply: false` plus a specific `description` so the agent can load only the topics relevant to the current action.

## Rule index

| File | Load when |
| --- | --- |
| `change-checklist.mdc` | Apply as a final Clean Code gate before shipping: names, size, side effects, tests, and scoped cleanup. |
| `primary-principles.mdc` | Apply as the Clean Code bias when choosing readability, Boy Scout cleanup, local reasoning, or long-term simplicity over cleverness. |
| `naming-rules.mdc` | Apply when naming classes, functions, variables, or modules; avoiding encodings, synonyms, and misleading identifiers. |
| `function-rules.mdc` | Apply when shaping functions: size, one thing, abstraction level, parameters, command/query separation, or nesting. |
| `comment-rules.mdc` | Apply when writing, keeping, or removing comments; prefer self-explanatory code over narrative comments. |
| `formatting-and-structure.mdc` | Apply when ordering files vertically, keeping related concepts close, or formatting for scannability. |
| `objects-modules-and-data-structures.mdc` | Apply when separating objects from data structures, hiding representation, or avoiding train-wreck chains. |
| `class-and-module-design.mdc` | Apply when keeping classes small and cohesive, shaping public APIs, or preferring composition. |
| `error-handling.mdc` | Apply when designing errors, keeping happy paths clear, or isolating error handling from main logic. |
| `boundaries-and-external-dependencies.mdc` | Apply when wrapping third-party APIs, isolating frameworks, or keeping boundary learning out of core logic. |
| `system-construction-rules.mdc` | Apply when assembling systems, delaying concrete decisions, or keeping construction separate from business logic. |
| `tests.mdc` | Apply when writing readable, fast, independent tests that document behavior. |
| `tdd-and-clean-test-rules.mdc` | Apply when following TDD cadence or keeping tests clean, FIRST, and free of duplication. |
| `concurrency-and-async-work.mdc` | Apply when introducing threads, async work, or shared mutable state that must stay understandable. |
| `refactoring-rules.mdc` | Apply when cleaning structure during change while keeping tests green and steps small. |
| `emergent-design-and-successive-refinement.mdc` | Apply when letting design emerge through successive refinement rather than speculative abstraction. |
| `smells-to-detect-and-eliminate.mdc` | Apply when hunting Clean Code smells: rigidity, opacity, duplication, feature envy, dead code, and related local decay. |
| `change-process.mdc` | Apply when applying the Boy Scout Rule, scoped cleanup, or change discipline on touched code. |
| `implementation-preferences.mdc` | Apply when choosing everyday implementation defaults for clarity, simplicity, and safe change. |

## Relationship to mini / nano / skill / subagent

- **Plugin skill** ([`../skills/clean-code/`](../skills/clean-code/)): loads `mini` by default for book-specific workflows.
- **Root skill entry** ([`../SKILL.md`](../SKILL.md)): Agent Skills CLI / portable entrypoint.
- **These rules**: split the **full** source for Cursor's intelligent, per-action attachment.
- **Subagent** ([`../agents/clean-code-reviewer.md`](../agents/clean-code-reviewer.md)): read-only audit in an isolated context.
- Prefer these over dumping the whole full file into an Always Apply rule. See [`../README.md`](../README.md).
