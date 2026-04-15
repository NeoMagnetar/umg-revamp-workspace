# BATCH-187 - Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
Topic: Stack versus domain language
Tension: Stack is mechanically locked, while domain is favored for human-facing grouping, but the language was still being stress-tested.
Why it matters: Human-facing docs can drift if terms are not frozen carefully.

## Flag 2
Topic: UI versus canon boundary
Tension: Nested snaps, graph crowding, zoom, collapse, and other UI mechanics remained conceptual rather than canonically finalized.
Why it matters: UI expression should not silently redefine core semantics.

## Flag 3
Topic: Explanatory vocabulary drift
Tension: Some explanatory phrases introduced during discussion may not all be desired as final canon.
Why it matters: Draft explanations can leak into formal docs if not cleaned.

## Flag 4
Topic: Nested snap implementation
Tension: Conceptual nested-snap inheritance was discussed but not fully encoded as final compiler behavior.
Why it matters: Compiler work needs explicit spec, not conceptual implication.

## Flag 5
Topic: Repo migration boundary
Tension: The old repo was recommended for archive while a fresh repo becomes authoritative, but migration and preservation details still require policy-level clarity.
Why it matters: Historical continuity and clean implementation can conflict without explicit migration rules.
