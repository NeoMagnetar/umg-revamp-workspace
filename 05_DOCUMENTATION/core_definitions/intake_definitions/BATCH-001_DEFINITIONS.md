# BATCH-001_DEFINITIONS

## Terminology Extraction
### Sleeve
- Proposed meaning in source: top-level runtime identity defining who the system is right now
- Stability in batch: strong
- Caution: evidence only; not canonized here

### Resleeving
- Proposed meaning in source: operational mechanism for switching runtime identity through load -> compile -> validate -> snapshot -> activate
- Stability in batch: strong

### Compiler
- Proposed meaning in source: current minimal translator that reads sleeve source, validates required fields, and emits normalized runtime spec
- Stability in batch: strong
- Caution: explicitly not final compiler maturity

### Source assets
- Proposed meaning in source: authoring-layer semantic/source materials prior to compilation

### Compiled assets
- Proposed meaning in source: machine-generated normalized runtime specification produced from source assets

### Active state
- Proposed meaning in source: live activated runtime state after compile/validate/snapshot/activate flow

### Block
- Proposed meaning in source: atomic meaning unit

### NeoBlock
- Proposed meaning in source: compiled active view of lower-level block material within a stack
- Stability in batch: medium; implementation depth deferred

### NeoStack
- Proposed meaning in source: domain-level or workmode-level aggregation of NeoBlocks
- Stability in batch: medium-high

## Role Language
### MOLT role family named in source
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint

### Role-language meaning
- These are treated as semantic roles, not interchangeable command labels.
- MOLT is positioned as an atomic classification layer under higher assemblies.

## Architecture Language
- layered system
- runtime identity
- compile / activate flow
- source semantics
- runtime activation
- active state
- deterministic / inspectable / reversible resleeving
- permissive operator posture
- bounded-agency branch
- output rendering separate from cognition

## Runtime / Compiler Language
- validate required fields
- normalized runtime spec
- explicit active sleeve state
- explicit active stack state
- state directories
- history / snapshots
- future MOLT parsing
- future NeoBlock generation
- future NeoStack expansion
- future conflict detection
- future merge / bundle logic

## Definitional Candidates
- Sleeves are runtime identity, not labels or prompt presets.
- Format/output rendering is separate from cognition.
- Source assets, compiled assets, and active state are separate layers.
- Resleeving should be deterministic, inspectable, and reversible.
- The current compiler is translator-first; deeper synthesis comes later.

## Definitional Cautions
- The source uses some “candidate canon language” framing internally; this intake pack preserves those as candidates only.
- Trigger, Priority, Merge, and Bundle are named, but their final semantics are not fixed by this batch alone.
