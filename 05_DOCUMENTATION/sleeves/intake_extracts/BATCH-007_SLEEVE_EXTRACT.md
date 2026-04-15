# BATCH-007 — Sleeve Extract
## Sleeve-Relevant Signals
- The existing design-focused base state is treated as the wrong default because it traps the system in one permanent mode.
- A new neutral base sleeve is proposed: `UMG_BASE` / `umg_base.core`.
- This base sleeve should be active, governed, and idle by default.
- It should not auto-execute, auto-mutate, auto-inspect, or auto-resleeve.
- Design, inspection, execution, mutation, and resleeving should be explicit subordinate modes or overlays under the base sleeve.
- The older design sleeve should be reframed as a subordinate/design sleeve rather than the global default.

## Candidate Sleeve Implications
- Base-sleeve docs should become explicit anchor artifacts for checks and operator understanding.
- Sleeve identity should remain static while MOLT maps carry current-turn activity.
- Neutral base posture reduces accidental mode lock-in and supports cleaner explicit activation.
- Future persona layers should be hosted on top of UMG substrate rather than replacing it as base identity.
