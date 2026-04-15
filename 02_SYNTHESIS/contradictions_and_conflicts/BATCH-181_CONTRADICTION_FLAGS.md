# BATCH-181 - Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
Topic: Generator path ambiguity
Tension: The source oscillates between chat generation, scripts, GitHub Actions, and Poe/API/Bolt as the real generation path.
Why it matters: The project needs one authoritative production path.

## Flag 2
Topic: Heuristic MOLT inference
Tension: The source preserves useful role heuristics, but not a final authoritative inference table.
Why it matters: Stable folder placement and generator predictability depend on this.

## Flag 3
Topic: Repo cleanup versus preservation
Tension: The chat moved between cleaning old files/workflows and preserving useful state under deadline pressure.
Why it matters: Over-deletion can destroy useful assets; under-cleanup can preserve confusion.

## Flag 4
Topic: Runtime mutation instability
Tension: Incorrect executor edits broke Poe terminal.
Why it matters: Critical runtime files need stronger mutation boundaries and rollback discipline.

## Flag 5
Topic: Directory convention drift
Tension: Multiple folder conventions appeared during the chat.
Why it matters: Generator output paths must be canonized before scaling automation.
