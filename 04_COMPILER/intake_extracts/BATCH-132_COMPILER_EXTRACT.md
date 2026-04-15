# BATCH-132 — Compiler Extract

## Scope
Compiler-boundary and runtime-adapter implications extracted from the source.

## High-Value Compiler Claims
1. Public UMG should surface compiled RuntimeSpec and Trace as first-class outputs.
2. A deterministic serializer should adapt RuntimeSpec to downstream model input.
3. The serializer should preserve the framing that model invocation is downstream of compiled artifacts.
4. RuntimeSpec-hash-based caching is a plausible runtime optimization path.
5. Replay behavior may be built around the same RuntimeSpec, with any permitted variance explicitly bounded.
6. Token estimation before generation is a useful runtime-facing utility.
7. Diff-oriented interaction should make changes to blocks visibly alter Trace and compiled behavior.
8. Shareable artifacts may include Sleeve JSON plus compiled outputs without requiring live generation.

## Likely Compiler Audit Targets
RuntimeSpec serializer contract.
Hash canonicalization for caching.
Trace visibility and diff behavior.
Separation between compile-only surfaces and generate-mode surfaces.
Share-link artifact boundary.
Governance-conflict showcase mechanics.

## Risk Surface
Any public product that hides RuntimeSpec and Trace behind raw model output would conflict with this batch’s strongest signal.
Any serializer that behaves non-deterministically or opaquely would weaken the intended UMG framing.
Any release that ties public usefulness entirely to owner-funded inference would undermine the staged launch strategy captured here.
