# BATCH-113 — Definitions Extract

## Terminology surfaced in this batch

### UMG Info Archive
A chat/archive space for gathering information from conversations so they can be compared over time.

### Artifact taxonomy / extraction outline
The categories gathered from each chat to make conversations parsable, comparable, and auditable.

### Archive object model
A versioned, diff-friendly machine-readable structure for storing chats, turns, artifacts, and conflicts.

### Artifact
An extracted typed unit such as a definition, rule, sleeve, block, analysis, or conflict.

### Conflict
A typed record that stores participants, evidence, severity, status, and possible resolution across archived artifacts.

### Conflict-detection pass
A deterministic stage that runs over archived artifacts to emit conflicts.

### Scope
Proposed archive scoping levels: global, chat, thread, turn, local.

## Role language and archive language

### Typed payload
A structured artifact record with required and optional fields rather than free-form prose only.

### Candidate
An ambiguity-preserving status for extracted material that should be retained without premature canonization.

### Authority decision
An archived record capturing governance override, priority resolution, scope override, deprecation, or similar supersession behavior.

### Constraint violation
A typed archived record describing a breached rule or incompatible condition.

### Lineage
A record of source artifacts, prior versions, or merge history preserved for diffability and traceability.

## MOLT-related representational signal
- MOLT-style fields appearing in archive-facing payloads:
  - trigger
  - directive
  - instruction
  - subject
  - primary
  - philosophy
  - blueprint
- Block payload template also proposed `block_type` values such as:
  - why
  - subject
  - directive
  - instruction
  - philosophy
  - blueprint
  - trigger
  - governance

## Unresolved definitional areas
- whether the archive schema is canonical or tool-only
- whether the runtime-style sleeve JSON is example, canon, or incidental template
- whether proposed scope levels are stable project terminology
- when automatic conflict resolution is permitted versus when manual review is required
