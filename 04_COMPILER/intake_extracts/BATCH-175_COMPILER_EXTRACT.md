# BATCH-175 — Compiler Extract

## Scope
Compiler- and implementation-facing implications extracted from the CSL/canon foundation source.

## High-Value Compiler Claims
1. Compiler input/output contract is repeatedly framed as:
   - input: Sleeve JSON
   - output: RuntimeSpec + Trace
2. Fixed compiler pipeline repeatedly specified:
   - parse
   - validate
   - choose snap
   - select snap blocks
   - remove Off
   - resolve stacks
   - apply triggers
   - enforce authority/directionality
   - merge
   - validate PrimaryShell
   - emit RuntimeSpec
   - emit Trace
3. Determinism is mandatory.
4. Trace must be chronological and consistent with final active blocks.
5. Trigger v0 is actions-only and should not evaluate conditions internally.
6. Merge is same-type only and keyed by same non-empty merge_key in the source’s stated rule set.
7. Stack resolution is same-type only and deterministic.
8. Compiler is the enforcing spine; without it, UMG is inert documentation.

## Likely Compiler Audit Targets
CSL-to-compiler contract formalization.
Compiler stage ordering.
Trigger v0 legality.
Stack-key and same-type resolution.
Merge-key and merge-policy normalization.
PrimaryShell validation requirements.
Trace consistency and event taxonomy.
Greenfield `umg-core` repo implementation path.
