# BATCH-201 — Definitions Extract

## Terminology
### Snap
Compatibility / adjacency relationship between MOLT types.

### Stack
Vertical hierarchy or grouped assembly represented in stack/sleeve files.

### Merge
Conflict resolution / precedence logic; semantically unresolved as a canonical type versus an operation/control concept.

### Deployment
Packaging / export / publish / final-mile logic; present operationally, but canon status remains unsettled.

### Canonical Block Tree
`data/blocks/{MOLT_TYPE}/*.block.json` as the single source of truth for blocks.

### Manifest
Generated file mapping canonical blocks into per-type or template import structures for builder use.

### Schema / Config Files
Files such as merge matrix, snap matrix, or web matrix that govern relationships rather than acting as content blocks.

## MOLT Role Language
### Primary
Root/core identity or plan anchor.

### Subject
Domain area or content target.

### Instruction
Execution logic or behavior rule.

### Philosophy
Tone / ethos / worldview layer.

### Blueprint
Layout / format / rendering logic.

### Directive
Strategic overlay or control logic.

### Trigger
Event-driven activation logic.

### Off
Disabled or suppressed logic / UI role.

## Sleeve / Builder Language
### Core Sleeve
Embedded/runtime sleeve living under `/poe_core/sleeves/`.

### User-Facing Stack / Sleeve
Template or stack bundle living under `/sleeves/`.

### Envoy
Persistent, code-first sub-agent that may later become a block, with Cantocore and trigger/language metadata.

## Definitional Candidates
- single-source-of-truth block architecture
- canonical per-block file model
- stacks reference block IDs only
- schema/config files govern relationships, not content
