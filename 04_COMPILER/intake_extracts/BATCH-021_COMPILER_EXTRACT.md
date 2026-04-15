# BATCH-021 — Compiler Extract

## High-Value Compiler Signals
- CyentCore should compile into canonical JSON/runtime form
- Compiler should shift from expansion-first to constraint-first
- Separate these validity layers:
  - structural validity
  - execution validity
  - dominance validity

## Candidate Compiler Hardening Work
- formal trigger-routing map
- compile-time prose conflict linting
- severity levels
- dependency graph checks
- diff validation
- canon freeze mode
- production hard-fail validation

## Merge / Dominance Signals
- merge precedence requires formal completion
- numeric `merge_rank` and dominance math still incomplete
- governance precedence must remain explicit and non-bypassable

## Staging Rule
- v2 = hardening and proof
- v3 = new atomic primitives / ontology expansion
- do not mix them
