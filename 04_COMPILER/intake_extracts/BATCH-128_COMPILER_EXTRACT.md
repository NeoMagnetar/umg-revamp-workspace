# BATCH-128 — Compiler Extract

## Scope
Compiler-facing semantic and implementation implications extracted from the source.

## High-Value Compiler Claims
1. Sleeve JSON is the authored source of truth.
2. Compiler-resolved truth is distinct from UI/editor state.
3. Priority applies only within same-MOLT peer collisions.
4. Priority does not cross MOLT lanes or override governance.
5. Governance is the only override mechanism.
6. Merge is a subset operation inside a stack, using declared result blocks.
7. Bundle records grouping/selection structure without automatically inventing new compiler blocks.
8. Whole-stack compression into a NeoBlock is distinct from subset bundle/merge behavior.
9. Editor-only intent and layout state should live under `sleeve.ui` / `sleeve.ui.ops`.
10. Deterministic outputs include RuntimeSpec and Trace, with timestamps/compiledAt noted as a remaining nondeterministic surface.
11. RuntimePromptSpec is a plausible next official output artifact.
12. Current compiler-v0 behavior, as summarized in the source, includes compileSleeve, validation, normalization, merges, bundles, governance, live filtering, authority resolution, per-type selection, NeoBlock/NeoStack building, and artifact generation.

## Likely Compiler Audit Targets
Formalize RuntimePromptSpec and artifact boundaries.
Document deterministic compile flow and failure conditions.
Verify current sequencing against intended sequencing.
Ensure priority remains same-bucket only.
Keep bundle/merge subset operations separate from NeoBlock compression.
Define hash or integrity output rules for reproducibility.
Preserve UI-only metadata isolation from compiler semantics.

## Risk Surface
Any UI that visually implies priority changes MOLT hierarchy would conflict with this batch.
Any compiler or editor flow that conflates subset bundle/merge with whole-stack NeoBlock compression would conflict.
Any runtime path that treats dead-shell client code as canonical product runtime would create staging confusion.
