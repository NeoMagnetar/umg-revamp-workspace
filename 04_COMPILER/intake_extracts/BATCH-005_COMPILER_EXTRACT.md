# BATCH-005 — Compiler Extract
## Compiler-Relevant Signals
- Align future sleeve/stacks JSON to the real compiler schema rather than ad hoc JSON.
- Preserve the compiler sequence: validate -> normalize -> merge -> bundle -> governance -> authority -> active selection -> runtime emission.
- Support explicit blueprint-selection / format-routing structures as compiler-friendly objects.
- Preserve deterministic compile order even when tag-driven or shorthand controls are introduced.
- Treat tag indexes, bundle intents, governance overrides, and active-block subsets as first-class validation surfaces.

## Candidate Compiler Tasks
- Add an explicit format-router / blueprint-selection model that does not collapse blueprint logic into cognition stacks.
- Define the canonical relation between shorthand authoring forms and strict compiler JSON.
- Harden validation for tag-index integrity, bundle intent/winner coherence, and governance-derived forbids/overrides.
- Clarify whether temporary list order can ever stand in for formal priority.

## Compiler Caution
This batch is grounded in real compiler behavior, but its operator-facing shorthand layer remains partially provisional and must not be mistaken for finalized compiler contract.
