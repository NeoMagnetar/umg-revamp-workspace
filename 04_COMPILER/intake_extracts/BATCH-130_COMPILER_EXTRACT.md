# BATCH-130 — Compiler Extract

## Scope
Compiler-facing implementation implications extracted from the source.

## High-Value Compiler Claims
1. The compiler takes Sleeve plus TriggerState and outputs RuntimeSpec plus Trace.
2. The compiler must remain deterministic, rule-enforcing, non-agentic, and must not call AI models in v0.
3. Trigger truth is not computed by the compiler in v0; active trigger IDs are passed in externally.
4. Governance is explicit and scoped through GovernanceRule and GovernanceBinding structures.
5. Authority and priority are distinct: authority governs override legality, while priority governs ordering within allowed levels.
6. Bundle and merge are the semantic compilation units via normalized segments.
7. Implicit or explicit singleton bundles may be used so the compiler sees normalized segments rather than loose stacked blocks.
8. Merge must preserve lineage and log it in Trace.
9. NeoBlock construction may arise from merge results or compressed stacks, but traceability and boundaries must be preserved.
10. An 11-step deterministic compile pipeline is proposed:
   - basic validation
   - register/log triggers
   - normalize segments
   - apply governance
   - resolve stacks
   - resolve merge segments
   - construct NeoBlocks
   - construct NeoStacks
   - select Primary
   - build RuntimeSpec
   - finalize Trace and result
11. Trace schema should include event types such as bundle_applied, merge_applied, governance_applied, conflict_resolved, trigger_considered, trigger_used_in_condition, error, and warning.
12. Error taxonomy should distinguish hard and soft failures.

## Likely Compiler Audit Targets
Segment normalization policy.
Implicit singleton bundle behavior.
Trigger input handling and trace logging.
Governance rule and binding application order.
Authority vs priority enforcement.
Per-MOLT merge/bundle policy rules.
NeoBlock and NeoStack construction boundaries.
Trace event completeness.
Error code consistency.
PRD-to-implementation parity.

## Risk Surface
Any implementation that blurs bundle with merge or UI collapse with semantic composition would conflict with this batch.
Any implementation that lets priority distort authority would conflict.
Any implementation that silently invokes AI or infers trigger truth inside the v0 compiler would conflict.
