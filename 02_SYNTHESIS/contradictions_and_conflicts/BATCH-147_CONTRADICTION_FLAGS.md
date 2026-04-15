# BATCH-147 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Uniform `Primary` assignment  
**Tension:** Every generated block was assigned `molt_type: "Primary"` without deeper role justification.  
**Why it matters:** The production default may not equal true semantic role classification.

## Flag 2
**Topic:** Placeholder `block_id` strategy  
**Tension:** `block_id` is described as hashable later, but no final identity policy was locked here.  
**Why it matters:** Large-scale library production needs stable identity guarantees.

## Flag 3
**Topic:** `canto_overlay` presence without depth  
**Tension:** The field exists structurally but remained semantically thin in the examples.  
**Why it matters:** Empty or weak fields can create schema bloat unless their role is clarified.

## Flag 4
**Topic:** Runtime claims versus implementation detail  
**Tension:** The source says blocks can appear in Sidebar, be dragged to Canvas, be merged, and be viewed in JSON, but no implementation detail is provided here.  
**Why it matters:** Product claims and protocol claims should remain distinguishable.

## Flag 5
**Topic:** Future extensibility signals  
**Tension:** Future `trigger`, `function_calls`, and AI instruction fields were mentioned, but not formalized in this batch.  
**Why it matters:** Expansion direction should not be mistaken for already-approved schema.
