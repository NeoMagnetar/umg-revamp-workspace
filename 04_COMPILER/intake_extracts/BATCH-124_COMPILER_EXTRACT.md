# BATCH-124 — Compiler Extract

## Scope
Compiler-relevant claims and implications extracted from the batch.

## High-Value Compiler Claims
1. Compiler is the deterministic transform pipeline; synthesis is a stage within that pipeline.
2. RuntimeSpec and Trace are the two core outputs.
3. TriggerState is explicit declared input rather than implicit world observation.
4. Governance may reference TriggerState during synthesis.
5. Priority is assigned, not inferred, and only operates within governance-permitted scope.
6. Priority cannot set OFF and cannot override governance.
7. Selection is per synthesis pass and does not permanently exclude non-selected elements.
8. OFF is explicit exclusion from synthesis.
9. Bundle order is structural evaluation order, not semantic authority.
10. Merge is explicit, deterministic, and traceable.
11. NeoBlocks are compiled resolved units.
12. Repeated synthesis / recompile snapshots are the clean explanation for dynamic reconfiguration.
13. Runtime host behavior is separate from normative spec behavior.
14. Some published spec semantics may exceed current compiler-v0 enforcement.

## Likely Compiler Audit Targets
TriggerState ingestion and pass-based recompilation model.
Governance OFF enforcement.
Trace completeness for governance, priority, bundle, merge, routing, and active-structure outcomes.
Deterministic governance-based priority assignment.
Selection-vs-OFF behavior.
Boundary between normative compiler behavior and runtime-host behavior.
Implementation-status note policy when spec exceeds tooling.

## Risk Surface
A compiler that treats non-selection as exclusion would conflict with this batch.
A compiler that lets priority override governance would conflict.
A documentation or tooling surface that blurs runtime-host behavior into the spec layer would conflict.
