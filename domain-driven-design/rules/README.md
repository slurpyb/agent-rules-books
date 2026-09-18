# Domain-Driven Design — Cursor Rules

Granular Cursor project rules distilled from the full source in [`../domain-driven-design.md`](../domain-driven-design.md).

These `.mdc` files are packaged with the `domain-driven-design` Cursor plugin (`rules/` is auto-discovered). Each rule uses **Apply Intelligently**: `alwaysApply: false` plus a specific `description` so the agent can load only the topics relevant to the current action.

## Rule index

| File | Load when |
| --- | --- |
| `change-checklist.mdc` | Apply as a final DDD gate: language, context, aggregates, invariants, and infrastructure separation. |
| `primary-directive-and-scope.mdc` | Apply when deciding whether DDD is warranted, preferring model clarity over CRUD/framework convenience, or rejecting ceremonial layering. |
| `knowledge-crunching-and-deep-models.mdc` | Apply when discovering domain concepts, deepening a shallow model, or treating awkward code as a modeling signal. |
| `model-driven-design.mdc` | Apply when aligning code, tests, and discussion language with the domain model. |
| `breakthrough-and-deeper-insight.mdc` | Apply when a better model appears and migration must stay incremental and behavior-preserving. |
| `making-implicit-concepts-explicit.mdc` | Apply when promoting hidden policies, constraints, or processes into named domain concepts. |
| `ubiquitous-language.mdc` | Apply when naming APIs, tests, and modules with domain expert vocabulary inside a bounded context. |
| `communication-artifacts.mdc` | Apply when keeping diagrams and docs lightweight, current, and tied to the implementation model. |
| `scenario-walkthroughs.mdc` | Apply when validating a model through concrete domain scenarios and examples. |
| `layered-architecture-and-smart-ui.mdc` | Apply when separating domain from UI/infrastructure or resisting Smart UI for complex domains. |
| `bounded-contexts.mdc` | Apply when defining, naming, or protecting a bounded context and its model boundary. |
| `strategic-design.mdc` | Apply when distinguishing core, supporting, and generic subdomains or drawing context maps. |
| `model-integrity-patterns.mdc` | Apply when choosing context relationships (shared kernel, customer/supplier, anticorruption layer, open host, etc.). |
| `distillation.mdc` | Apply when distilling the core domain and isolating supporting/generic complexity. |
| `large-scale-structure.mdc` | Apply when imposing large-scale structure across many contexts without erasing local models. |
| `strategic-decision-making.mdc` | Apply when prioritizing modeling investment where business differentiation is highest. |
| `entities.mdc` | Apply when modeling identity, lifecycle, and continuity with entities. |
| `value-objects.mdc` | Apply when modeling values by attributes, immutability, and replaceability rather than identity. |
| `associations-and-modules.mdc` | Apply when constraining associations and packaging the model into coherent modules. |
| `aggregates.mdc` | Apply when choosing aggregate boundaries, roots, and transactional consistency rules. |
| `domain-services.mdc` | Apply when placing domain behavior that does not naturally belong on an entity or value object. |
| `explicit-concepts-and-specifications.mdc` | Apply when modeling policies, specifications, or explicit domain rules as first-class concepts. |
| `repositories.mdc` | Apply when retrieving aggregates, preserving model access patterns, or avoiding leaking persistence into the domain. |
| `factories.mdc` | Apply when encapsulating complex creation while protecting invariants. |
| `application-layer.mdc` | Apply when shaping application services as orchestration without burying domain rules. |
| `infrastructure.mdc` | Apply when isolating persistence, messaging, and framework details from the domain model. |
| `translation-at-boundaries.mdc` | Apply when translating between bounded contexts without contaminating models. |
| `supple-design.mdc` | Apply when making the model intention-revealing, side-effect-free where practical, and easier to combine. |
| `analysis-and-model-patterns.mdc` | Apply when reusing analysis/model patterns without forcing them where they do not fit. |
| `code-generation-rules.mdc` | Apply when generating domain code that must express language, boundaries, and invariants correctly. |
| `review-rules.mdc` | Apply when reviewing domain changes for language drift, boundary leaks, or anemic models. |
| `testing-rules.mdc` | Apply when testing domain behavior, invariants, and scenario examples rather than persistence plumbing. |
| `forbidden-patterns.mdc` | Apply when spotting fake DDD, anemic domain models, context mush, or infrastructure-driven design. |
| `refactoring-rules.mdc` | Apply when refactoring toward a deeper model in safe steps inside a context. |
| `output-expectations.mdc` | Apply when producing DDD design or implementation output that must state language, context, and invariants explicitly. |

## Relationship to mini / nano / skill / subagent

- **Plugin skill** ([`../skills/domain-driven-design/`](../skills/domain-driven-design/)): loads `mini` by default for book-specific workflows.
- **Root skill entry** ([`../SKILL.md`](../SKILL.md)): Agent Skills CLI / portable entrypoint.
- **These rules**: split the **full** source for Cursor's intelligent, per-action attachment.
- **Subagent** ([`../agents/ddd-reviewer.md`](../agents/ddd-reviewer.md)): read-only audit in an isolated context.
- Prefer these over dumping the whole full file into an Always Apply rule. See [`../README.md`](../README.md).
