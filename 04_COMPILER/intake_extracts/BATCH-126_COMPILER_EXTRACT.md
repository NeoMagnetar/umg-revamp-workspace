# BATCH-126 — Compiler Extract

## Scope
Compiler-relevant rules and implications extracted from the source.

## High-Value Compiler Claims
1. Compiler input is Sleeve.
2. Compiler outputs are RuntimeSpec and Trace.
3. Compiler should be deterministic, non-generative, model-agnostic, and audit-oriented.
4. `stack_rank` should be removed and replaced with `priority_group`.
5. Priority is categorical, not numeric, and only applies among peers in the same scope and resolution context.
6. MOLT authority must remain distinct from priority.
7. Attachment affects scope of application, not authority.
8. Bundle and merge require distinct codepaths.
9. Merge across MOLT areas is only legal as structured runtime assembly or explicit typed derivation.
10. UI actions must emit explicit metadata rather than hidden semantics.
11. Compiler pipeline should include validation, normalization, off handling, attachment handling, bundle/merge resolution, authority enforcement, explicit synthesis, runtime build, canonicalization, stable hash generation, and Trace emission.
12. Trace must record validation, bindings, off-state removals, bundle ordering, merge decisions, synthesis provenance, runtime build, and final hash.

## Likely Compiler Audit Targets
Removal of `stack_rank` from schemas and logic.
Implementation of categorical `priority_group`.
Explicit bundle vs merge resolution paths.
Attachment resolution model.
Canonicalized RuntimeSpec output and stable hashing.
Trace event schema completeness.
Normalized types for Block, Column, NeoBlock, NeoStack, and Sleeve.
MergeOps and typed derive behavior if included.

## Risk Surface
The batch contains some tension with evidence that assigns override power solely to governance rather than to MOLT hierarchy.
NeoStack default compose mode remains unresolved.
Governance semantics remain underdefined enough that compiler staging should not over-assume.
