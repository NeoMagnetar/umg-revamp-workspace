# BATCH-108 — Contradiction Flags

## Flag 1 — Graph freedom vs semantic hierarchy
- **Signal A:** Graph-style canvas suggests free node movement and unconstrained connections.
- **Signal B:** UMG requires rooted, ordered structure with Primary at the top and no upward placement above it.
- **Why it matters:** Generic graph freedom can erase UMG semantics if left unbounded.
- **Follow-up needed:** Define the hard constraints the graph runtime must enforce.

## Flag 2 — `Deployment` as an active builder-facing role
- **Signal A:** This batch includes Deployment in the wizard/role set.
- **Signal B:** Other intake packets question Deployment as a valid main MOLT role.
- **Why it matters:** Builder taxonomy may drift from broader core-alignment work.
- **Follow-up needed:** Decide whether Deployment remains a role, becomes metadata, or is recast.

## Flag 3 — Merge UX remains underdefined
- **Signal A:** Side-drop should attempt merge/overlay.
- **Signal B:** Manual merge controls and undo were also proposed.
- **Why it matters:** Runtime behavior, user expectations, and save-state semantics all depend on this choice.
- **Follow-up needed:** Choose between auto-merge, confirm-merge, or hybrid confirmation rules.

## Flag 4 — Code reality vs planning language
- **Signal A:** Earlier plans proposed implementation files and structure from scratch.
- **Signal B:** Later discussion revealed a more advanced existing `GraphCanvas.tsx`, making some earlier guidance partially stale.
- **Why it matters:** Recovery work must patch live code rather than overwrite it with obsolete scaffolding.
- **Follow-up needed:** Establish current-code truth before applying further builder patches.

## Flag 5 — Top-level plan categories not yet locked
- **Signal A:** Business plan, web app, and chatbot are treated as top-level modes.
- **Signal B:** Exact category sets per plan type were not finalized.
- **Why it matters:** Library UX, manifest loading, and block discoverability depend on stable category structure.
- **Follow-up needed:** Lock category sets separately from MOLT runtime behavior.
