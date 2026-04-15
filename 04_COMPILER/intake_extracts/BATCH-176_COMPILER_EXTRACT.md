# BATCH-176 — Compiler Extract

## Scope
Compiler- and implementation-facing implications extracted from the documentation/semantics source.

## High-Value Compiler Claims
1. Canonical input remains Sleeve JSON.
2. Canonical outputs remain RuntimeSpec + Trace.
3. Repeated compiler pipeline:
   - parse sleeve
   - validate sleeve basic
   - choose snap
   - select snap blocks
   - remove Off blocks
   - resolve stacks
   - apply triggers
   - apply hierarchy / directionality
   - merge same-type groups
   - validate exactly one PrimaryShell
   - emit RuntimeSpec + Trace
4. Determinism is mandatory.
5. Authority order is global and non-configurable.
6. Trigger v0 remains actions-only and must not evaluate conditions internally.
7. Validation strictness, deterministic sort keys, exact ID strategy, snap schema, trigger action objects, compile failure behavior, and schema flexibility are all identified as pre-coding lock decisions.
8. TypeScript + Node + Vitest remain the preferred v0 implementation path.

## Likely Compiler Audit Targets
Exact compiler-stage sequencing.
PrimaryShell uniqueness validation.
Trigger action schema.
Deterministic sort and arbitration keys.
Difference between structural merge and creative synthesis.
Migration strategy for old repo semantics.
Strict-vs-flexible validation boundaries.

## Risk Surface
Any coding effort that starts before the remaining pre-coding lock decisions are normalized risks baking naming drift and semantic mismatch into the first compiler implementation.
Any implementation that blurs RuntimeSpec with prompt rendering would directly conflict with this batch’s strongest separation rule.
