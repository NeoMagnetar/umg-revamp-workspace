# BATCH-179 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Fresh repo versus in-place repair  
**Tension:** The conversation moved between repairing the current repo and rebuilding from a cleaner new baseline before leaning toward fresh-repo seeding.  
**Why it matters:** Migration doctrine should be explicit.

## Flag 2
**Topic:** Export keep-rules not finalized  
**Tension:** The curated package/export step is central, but exact keep/exclude rules were not locked.  
**Why it matters:** Package quality and rebuild trust depend on these rules.

## Flag 3
**Topic:** Envoy implementation incompleteness  
**Tension:** Envoys are conceptually clear, but actual production implementation remains provisional.  
**Why it matters:** Workflow clarity is ahead of code certainty.

## Flag 4
**Topic:** Repo-doc schema provisional  
**Tension:** `overview.yml`, `depgraph.yml`, and `todo.yml` were proposed as core inputs, but their exact schemas were not finalized.  
**Why it matters:** Later automation depends on stable documentation artifacts.

## Flag 5
**Topic:** History preservation unresolved  
**Tension:** How much history or legacy material should migrate into the new repo remained open.  
**Why it matters:** Clean rebuilds and continuity goals may conflict without explicit policy.
