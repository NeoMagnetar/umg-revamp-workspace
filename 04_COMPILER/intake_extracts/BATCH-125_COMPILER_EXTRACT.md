# BATCH-125 — Compiler Extract

## Scope
Compiler- and runtime-adjacent implications extracted from the source.

## High-Value Compiler / Runtime Claims
1. Tutorial flow behaves like a lightweight compile pipeline: compress → compose → name → sleeve → compile.
2. RuntimeSpec + Trace outputs are already present at the UI/output surface.
3. Hydration reportedly recomputes state deterministically.
4. PriorityOrder exists in schema and validation but is not yet fully integrated into composition/runtime decisions.
5. Merge and bundle remain underdefined and partially conflated in the current implementation.
6. NeoBlock snapshot structure has started to formalize by storing sourceBlockIds and MOLT snapshot data.
7. Gating and validation act as proto-governance behavior, though not yet as a formal governance subsystem.
8. Multi-layer mutation without trace destabilizes the system and should be treated as a process/compiler discipline failure.
9. Static deployment and feature freeze are preferred for the current release target.

## Likely Compiler Audit Targets
Formalize NeoBlock snapshot structure.
Differentiate bundle and merge semantics in compile output and trace.
Decide whether priority participates only after governance/scope determination.
Define explicit governance layer instead of relying on ad hoc gating.
Check whether hydration determinism and trace completeness are actually enforced.
Clarify compiler boundary versus UI-state orchestration.

## Risk Surface
Any implementation that mutates structure across multiple layers without trace checkpoints is at elevated regression risk.
Any release path that treats partial implementation semantics as settled canon risks documentation and compiler drift.
