# BATCH-125 — Contradiction Flags

## Flag 1 — Merge vs Bundle Ambiguity
The source says merge and bundle are both present but not deeply distinguished in the implementation.
This conflicts with any stronger semantic separation expected elsewhere unless clearly marked as incomplete tooling behavior.

## Flag 2 — Priority Defined but Not Operational
PriorityOrder is present in schema and inspector usage, but the source states it is not fully integrated into runtime semantics.
This creates a spec-to-implementation gap risk.

## Flag 3 — Governance Implied but Not Formalized
Tutorial gating and disabled actions behave like governance, yet the batch states there is no explicit governance block/system.
This should not be silently interpreted as full governance implementation.

## Flag 4 — Trigger Logic in State Machine Rather Than Authored Trigger Blocks
Trigger behavior appears in tutorial-step state transitions rather than explicit authored Trigger-block semantics.
Useful implementation detail, but not necessarily equivalent to canonical Trigger handling.

## Flag 5 — Candidate Vocabulary Scope
“Baseline sleeve,” “trace gate,” and “spine blocks” are valuable phrases, but this batch does not prove they are already normalized UMG canon.
Treat as candidate vocabulary only.

## Flag 6 — Mobile / ReactFlow Stability Unresolved
The batch explicitly documents unresolved rendering architecture and mobile support instability.
Any release or docs work should preserve that unresolved status.
