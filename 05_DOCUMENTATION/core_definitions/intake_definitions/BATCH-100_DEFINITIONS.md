# BATCH-100_DEFINITIONS

## Scope Note
These definitions are extracted from a derived source summary. They are evidence candidates, not canon.

## Terminology Extract

### Block JSON schema
- Structured block representation with fields reported as:
  - `id`
  - `type`
  - `cantocore`
  - `version`
  - `inputs`
  - `outputs`
  - `metadata`

### CompileMOLT
- Compiler surface described as converting Cantocore into normalized JSON.

### MOLT-Graph Runtime
- Runtime surface described as executing block graphs deterministically with memo caching.

### memo caching
- Execution optimization concept where repeated graph results are reused rather than recomputed.

### open-core
- Product/governance posture in which a permissively licensed core is paired with additional proprietary or selectively licensed surfaces.

### Patent Non-Assertion Pledge
- Proposed governance posture where compliant forks or ecosystem participants are protected from aggressive patent assertion.

## Role Language

### Primary
- Reported as an enumerated block type within the first-release schema.

### Subject
- Reported as an enumerated block type within the first-release schema.

### Instruction
- Reported as an enumerated block type within the first-release schema.

### Merge
- Reported as an enumerated block type within the first-release schema.

### Overlay
- Reported as an enumerated block type within the first-release schema and implied presentation/behavior layering surface.

## Architecture Language

### 5-block stack
- Starter visual-editor unit where users assemble small stack compositions through drag-and-drop behavior.

### starter library
- First-release set of named reusable blocks intended to seed practical use cases and demos.

### graph execution
- Runtime model where blocks are executed as graph-connected units rather than as only a flat sequence.

## Runtime / Compiler Language

### normalized JSON
- Compiler target form produced from Cantocore and used as a more stable runtime/persistence structure.

### persistence schemas
- Storage models named for:
  - `blocks`
  - `stacks`
  - `versions`

### hot reload
- Editor/runtime behavior where changes are reflected quickly without full restart, reported here as WebSocket-driven.

### acceptance tests
- Candidate compiler/runtime validation surface for CompileMOLT and graph-execution behavior.

## Governance / Release Language

### Apache 2.0 OSS core
- Governance baseline where the UMG core is permissively open-source.

### defensive patent strategy
- Strategy where IP is used primarily as a moat and ecosystem-protection instrument rather than only exclusionary control.

### phase gate
- Release-management checkpoint used to constrain scope and validate readiness before proceeding to later stages.
