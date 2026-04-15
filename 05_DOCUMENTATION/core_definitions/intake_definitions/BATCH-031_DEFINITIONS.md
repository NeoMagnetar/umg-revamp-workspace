# BATCH-031 — Definitions Extract

## Terminology
### NeoStack
- domain-level aggregation of distinct NeoBlocks
- should not collapse into one oversized reasoning blob

### NeoBlock
- functional unit inside a stack with role integrity preserved across Trigger, Directive, Instruction, Subject, Primary, Philosophy, and Blueprint

### Trigger
- activation gate
- should not act as authority-bearing decision maker
- should be expressed with detector refs and machine-readable logic rather than free prose

### Detector Ref
- normalized machine-readable reference used to express trigger or bundle activation conditions

### Bundle Expression
- formal activation expression over detector refs, context tags, or classifier outputs
- replacement for informal natural-language activation notes

### Merge Contract
- formal runtime rule set governing:
  - persistence vs ephemerality
  - reuse as later merge inputs
  - override behavior
  - dedupe behavior
  - parent requirements
  - activation timing
  - traceability

### Subject Arbitration
- stack-level rule for resolving subject behavior when multiple NeoBlocks activate

### Authority Enum
- normalized closed vocabulary for authority semantics
- should not mix inconsistent labels like HIGH / MEDIUM-HIGH / SUPREME / medium-low

### Whitepaper-Grade
- conceptually strong descriptive architecture
- not yet normalized enough for deterministic compiler/runtime use

### Runtime-Grade
- exact counts, normalized enums, machine-readable conditions, formal contracts, and testable behavior present

### DRAFT_ACCEPTED
- conditionally admitted draft status
- conceptually strong and worth retaining, but not yet compiler-ready

### COMPILER_READY
- normalized enough for deterministic compiler/runtime handling and validation-grade testing

## Role Language
- Trigger = activation gate
- Priority = role precedence + within-role ordering + deterministic tie-break
- Philosophy = coherent interpretive stance, but may remain decorative unless runtime effect is defined

## Architecture Language
- six-block causal split:
  - chain mapping
  - feedback detection
  - root analysis
  - correlation filtering
  - mechanism modeling
  - intervention simulation

## Runtime / Compiler Language
- lexical triggers alone are brittle
- use lexical candidates + intent classifier / pre-pass confirmation
- inventories, bundle conditions, merge policy, subject arbitration, and tests must be explicit
