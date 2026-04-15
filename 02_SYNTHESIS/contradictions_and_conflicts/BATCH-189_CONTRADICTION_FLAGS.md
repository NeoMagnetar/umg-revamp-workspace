# BATCH-189 - Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
Topic: Legacy versus current MOLT taxonomy
Tension: Legacy materials expose a concrete 9-role taxonomy and fixed hierarchy, while current retrieved public v0 materials require roles without publicly pinning the full table.
Why it matters: Canon vocabulary cannot remain ambiguous here.

## Flag 2
Topic: Merge semantics
Tension: Legacy repo treats Merge as a block type; current public framing treats merge as an explicit composition operation.
Why it matters: Migration guidance must be explicit.

## Flag 3
Topic: Trigger activation semantics
Tension: Legacy activation language uses Trigger block plus runtime_behavior_flags.is_active; current public-facing framing uses TriggerState plus synthesis rerun and governance/OFF.
Why it matters: Activation semantics need normalization.

## Flag 4
Topic: Sleeve / NeoStack / NeoBlock terminology
Tension: These are strong internal/ecosystem concepts but not fully pinned as canonical public v0 terms in retrieved sources.
Why it matters: Public docs need either stabilization or de-emphasis.

## Flag 5
Topic: README/spec/tooling mismatch
Tension: The public README appears broader than the visible retrieved repo tree and visible tooling coverage.
Why it matters: Users may misunderstand what is currently implemented versus planned.
