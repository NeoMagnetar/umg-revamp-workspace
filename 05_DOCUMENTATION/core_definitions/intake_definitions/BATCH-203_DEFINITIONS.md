# BATCH-203 — Definitions Extract

## Terminology
### Canon
Authoritative source of truth stored outside the model.

### Mapping
Visualization / structure workspace used to inspect, organize, and reason about canon.

### Runtime
Execution / reasoning surface that selectively loads fragments of canon.

### Selective Runtime Projection
Principle that runtime receives only the specific sleeves/blocks/stacks needed, not the full canon.

### One-Object-Per-File Model
Storage approach where each sleeve, block, or stack is stored as its own versioned file.

## Object Language
### Block
Functional unit with structured metadata and dependency references.

### Sleeve
Execution context or lens that links and orchestrates blocks.

### Stack
Compositional grouping/load surface above blocks; still shallowly defined in this source.

## Schema / Governance Language
### YAML Frontmatter
Suggested metadata surface carrying fields such as id, type, role, priority, tags, dependencies, and runtime metadata.

### Loader Protocol
Conceptual import-like mechanism for explicitly loading objects by ID and marking missing definitions.

### Hash Integrity
Optional governance enhancement such as sha256 for object verification.

## Definitional Candidates
- UMG must exist outside the model.
- Chat is execution. Repo is reality.
- Selective runtime projection.
- Canon / Mapping / Runtime.
