# BATCH-100_COMPILER_EXTRACT

## Scope
Compiler/runtime-relevant signals extracted from BATCH-100.

## High-Signal Candidates

### 1. CompileMOLT as Cantocore normalization boundary
The source explicitly frames CompileMOLT as converting Cantocore into normalized JSON.

This pressures UMG to specify:
- canonical grammar accepted by CompileMOLT
- normalization rules for block types and fields
- validation behavior for malformed or partial Cantocore
- stable compiler output contracts for downstream runtime use

### 2. Deterministic graph execution
The batch describes a MOLT-Graph Runtime that executes block graphs deterministically with memo caching.

Compiler/runtime questions:
- is the primary execution model graph-first, sequence-first, or hybrid
- how are dependency edges represented in normalized JSON
- what guarantees deterministic ordering when multiple paths are valid
- where memo keys and invalidation rules live

### 3. Persistence schemas for blocks, stacks, and versions
The source explicitly names persistence surfaces:
- `blocks`
- `stacks`
- `versions`

Potential implementation consequence:
- version-aware stack resolution
- rollback/audit paths
- compile cache coupling to versioned block artifacts
- migration logic as schema evolves from v0.1 onward

### 4. Acceptance-test pressure
The batch names CompileMOLT and MOLT-Graph Runtime acceptance tests as high-value candidates.

Suggested test surfaces:
- compile known Cantocore input into normalized JSON
- reject invalid block/type structures cleanly
- execute known graph topologies deterministically
- verify memo caching does not change correctness
- verify persistence snapshots resolve consistent runtime state

### 5. Vector layer integration
Qdrant is named as a vector-DB layer.

Compiler/runtime questions:
- is retrieval part of Merge semantics or separate runtime infrastructure
- how does vector recall feed graph execution
- what metadata/schema fields are required for retrievable blocks
- how should cached runtime state interact with retrieval freshness

## Suggested Audit Angles
- lock the CompileMOLT input/output contract for Spec v0.1
- define graph edge representation and deterministic ordering rules
- specify memo-cache keys, invalidation, and traceability
- formalize persistence schema responsibilities
- clarify where retrieval/vector behavior enters the runtime pipeline

## Confidence
High for planning signal, medium for finalized implementation status.
The batch is unusually concrete about compiler/runtime targets, but still reports a plan rather than verified shipped behavior.
