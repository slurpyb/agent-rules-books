# The Pragmatic Programmer — Cursor Rules

Granular Cursor project rules distilled from the full source in [`../the-pragmatic-programmer.md`](../the-pragmatic-programmer.md).

These `.mdc` files are packaged with the `the-pragmatic-programmer` Cursor plugin (`rules/` is auto-discovered). Each rule uses **Apply Intelligently**: `alwaysApply: false` plus a specific `description` so the agent can load only the topics relevant to the current action.

## Rule index

| File | Load when |
| --- | --- |
| `primary-directive.mdc` | Making engineering tradeoffs or choosing outcome-driven judgment |
| `core-principles.mdc` | Owning a change, maintainability beyond a local edit, quality/entropy |
| `dry-knowledge.mdc` | Duplicated business rules, validation, mappings, or process knowledge |
| `orthogonality.mdc` | Module boundaries, hidden coupling, overlapping responsibilities |
| `tracer-bullets.mdc` | New capabilities, architecture validation, end-to-end slices |
| `reversibility-and-requirements.mdc` | Vendor/platform commitments, domain languages, real requirements |
| `prototyping.mdc` | Spikes, experiments, proofs of concept |
| `automation.mdc` | Repeated build/test/release/setup steps |
| `feedback-loops.mdc` | Shortening change-to-signal time |
| `design-by-contract.mdc` | Preconditions, invariants, assertions, impossible states |
| `error-handling.mdc` | Detecting, classifying, and recovering from failures |
| `naming-and-communication.mdc` | Naming, comments, docs, communicating intent |
| `text-and-data.mdc` | Config/serialization formats, inspectable text vs lock-in |
| `state-and-concurrency.mdc` | Shared mutable state, async, concurrency assumptions |
| `estimation-and-increments.mdc` | Planning, estimating, small deliverable increments |
| `tooling.mdc` | Toolchain, generators, debugging discipline |
| `resources-and-coupling.mdc` | Resource ownership, Demeter, temporal coupling, growth |
| `project-and-team.mdc` | Team process, expectations, craft, ceremony skepticism |
| `broken-windows.mdc` | Small quality decay in touched code |
| `code-review.mdc` | Reviewing diffs/PRs for pragmatic smells |
| `forbidden-patterns.mdc` | Cargo-cult process, duplication, manual-everything, fossilized prototypes |
| `code-generation.mdc` | Generating or scaffolding new code |
| `testing.mdc` | Writing or running automated tests |
| `change-checklist.mdc` | Final gate before shipping a change |

## Relationship to mini / nano / skill

- **Skill** ([`../SKILL.md`](../SKILL.md)): loads `mini` by default for book-specific workflows.
- **These rules**: split the **full** source for Cursor's intelligent, per-action attachment.
- Prefer these over dumping the whole full file into an Always Apply rule.
