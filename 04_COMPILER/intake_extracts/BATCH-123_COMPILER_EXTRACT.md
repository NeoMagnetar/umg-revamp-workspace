# BATCH-123 — Compiler Extract

## Scope
Compiler-relevant rules and implications extracted from the source.

## High-Value Compiler Claims
1. UMG compiles authored cognitive structures into RuntimeSpec and Trace.
2. MOLT order is fixed semantic precedence, not automatic override or deletion.
3. Hierarchy orders influence; governance alone resolves disagreement.
4. Blocks are never implicitly modified or removed.
5. Bundle preserves grouping and priority without changing semantics.
6. Merge is explicit, traceable, and requires a result block.
7. Off excludes a block from compilation while preserving it for later reactivation.
8. Snap has no compiler semantics.
9. Scope is the explicit compiler-evaluated set.
10. NeoBlock is the compiled representation of one resolved Molt Stack.
11. NeoStack is a domain grouping with no intrinsic authority.
12. Compiler emits RuntimeSpec plus Trace.
13. Trace is mandatory for UMG validity.
14. Determinism requires stable ordering, explicit rules, and no hidden randomness.

## Likely Compiler Audit Targets
Parser handling of fixed MOLT order.
Normalization of type vs role.
Suppression logic to ensure hierarchy alone does not remove blocks.
Governance implementation as sole override layer.
Bundle representation vs merge representation in trace output.
Off-state exclusion behavior.
Scope derivation independent of UI relationships such as Snap.
NeoBlock and NeoStack construction boundaries.
Trace completeness and determinism guarantees.

## Risk Surface
Any existing implementation that treats vertical hierarchy as automatic suppression would conflict with this source.
Any implementation that gives Snap semantic meaning would conflict.
Any implementation that performs implicit merging, deletion, or non-traced suppression would conflict.
