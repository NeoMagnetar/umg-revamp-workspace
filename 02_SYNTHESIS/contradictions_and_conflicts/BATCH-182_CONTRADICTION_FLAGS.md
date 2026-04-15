# BATCH-182 - Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
Topic: Framework versus Builder boundary
Tension: The source carefully separates UMG from UMG Builder, but implementation detail volume could still cause Builder logic to be mistaken for framework canon.
Why it matters: Docs and decisions must keep this boundary explicit.

## Flag 2
Topic: Meta category status
Tension: Meta is useful in the Builder/runtime chat, but may remain a provisional extension rather than a canonical MOLT role.
Why it matters: Later canon work should not silently absorb it without review.

## Flag 3
Topic: Repo-state ambiguity
Tension: Local repo, GitHub-only files, generated packs, and stub-generated references drifted during the work.
Why it matters: Trustworthy staging and migration require explicit reconciliation.

## Flag 4
Topic: Final artifact counts
Tension: Some packs and folders were repaired under time pressure without one final definitive audit.
Why it matters: Release-readiness claims should remain measured.

## Flag 5
Topic: Builder completeness versus framework completeness
Tension: The chat explicitly preserves this distinction, but the existence of a near-term Bolt deliverable can blur it.
Why it matters: The project should not equate Builder readiness with full UMG readiness.
