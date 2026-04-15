# BATCH-099_COMPILER_EXTRACT

## Scope
Compiler/runtime-relevant signals extracted from BATCH-099.

## High-Signal Candidates

### 1. Explicit priority hierarchy
The source states a concrete ordering:
- Trigger > Directive > Instruction > Subject > Primary > Merge > Philosophy > Blueprint > Off

This pressures UMG to specify:
- whether this is compile-time ordering, runtime conflict resolution, or both
- how ties inside the same role are resolved
- whether Merge is always lower than Primary or only lower in some contexts
- how Blueprint and Philosophy interact when output shape conflicts with alignment language

### 2. Trigger evaluation and Off filtering
The source reports runtime logic including:
- trigger evaluation
- inactive / Off filtering
- condition-based execution

Compiler/runtime questions:
- what trigger vocabulary is canonical
- when Off is removed versus merely marked inactive
- whether trigger evaluation occurs before merge injection or after stack assembly
- how trigger events are surfaced to tooling and audit logs

### 3. Merge as context/data injection
Merge is described as injecting:
- external data
- memory
- retrieval results
- context

Potential implementation consequence:
- merge-source normalization
- scope rules for retrieval versus persistent memory
- conflict handling between merged context and existing stack instructions
- provenance retention for merged content

### 4. Overlay + sequential composition logic
The source combines vertical and horizontal snapping with overlay and sequence language.

This pressures UMG to define:
- overlay precedence versus sequence precedence
- whether horizontal snap rewrites, shadows, or annotates existing blocks
- how bundle/export serialization preserves those relationships

### 5. Export bundle construction
The source describes ZIP/JSON/markdown/runtime-marker output behavior.

Potential implementation consequence:
- canonical serialized project shape
- per-file export routing
- inclusion/exclusion rules for inactive logic
- executor-facing metadata for Bolt-style or other runtime consumers

## Suggested Audit Angles
- determine exact semantics of the stated priority hierarchy
- formalize trigger evaluation order and Off filtering behavior
- normalize merge-source and provenance rules
- define overlay versus sequential composition semantics
- standardize export bundle structure and runtime markers

## Confidence
Medium-high.
The source provides concrete runtime claims, but the implementation state and exact semantics remain partly unverified because the batch is a derived summary.
