# BATCH-152 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Shell proxy versus richer RPC actions  
**Tension:** The chat proposed both shell execution and future file/action APIs, but did not settle the final bridge surface.  
**Why it matters:** Interface shape affects safety, observability, and product simplicity.

## Flag 2
**Topic:** Cloud preview versus local/prod runtime  
**Tension:** Early assumptions relied on Docker-backed IDE runtime, but Bolt preview does not support nested Docker the same way.  
**Why it matters:** Runtime-mode awareness is mandatory.

## Flag 3
**Topic:** High autonomy versus bounded control  
**Tension:** The desired system should feel low-friction and agent-capable, but safety depends on whitelists, scoping, auth, and logging.  
**Why it matters:** Product convenience and control discipline need a clear balance.

## Flag 4
**Topic:** Indirect UMG relevance  
**Tension:** The source is useful to UMG, but it was not itself an explicit UMG design session.  
**Why it matters:** Later synthesis should preserve this as adjacent runtime architecture evidence, not direct canon law.

## Flag 5
**Topic:** Final security model unresolved  
**Tension:** Password gating, OAuth/JWT, workspace isolation, network policy, and resource limits were all proposed, but no final model was locked.  
**Why it matters:** Security posture should not be overstated.
