# BATCH-028 — Definitions Extract

## Terminology
### Sleeve
- router / governor layer
- classifies and routes before execution
- constrains scope and compiles execution packets

### NeoStack / Neostack
- executable task mode
- activated after trigger resolution
- expected to have explicit purpose, scope, outputs, and model-binding behavior

### NeoBlock
- compositional unit inside a neostack
- should be composed from canonical MOLT atoms already in the project
- should avoid invented identifiers where canonical IDs exist

### MOLT atom / block
- known reusable canonical unit in the project/GitHub library
- used as the reference substrate for NeoBlock composition

### Trigger
- first routing gate before execution
- should be deterministic and compiler/tool resolvable
- should not rely on random numbering when canonical trigger blocks are available

## Role Language
- sleeve = router/governor
- neostack = executable mode
- NeoBlock = compositional execution unit
- trigger = routing gate

## Architecture Language
- **Block -> NeoBlock -> NeoStack -> Sleeve**
- clean routing chain:
  - Trigger
  - Neostack
  - Directive
  - Instruction
  - Execution
  - Verify
  - Report

## Runtime / Compiler Language
- model binding at stack entry
- deterministic routing
- auditable transitions
- canonical ID reuse
- identifier normalization
- compiler-aligned spec

## Definitional Candidates
- Use existing MOLT blocks from the GitHub/project library, not invented or randomly numbered ones.
- Build NeoStacks as compositions of known MOLT atoms, not ad-hoc structures.
- Maintain clean routing: Trigger -> Neostack -> Directive -> Instruction -> Execution -> Verify -> Report.
