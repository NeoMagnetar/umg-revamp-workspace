# BATCH-105_DEFINITIONS

## Scope Note
These definitions are extracted from a derived source summary. They are evidence candidates, not canon.

## Terminology Extract

### UMG Block
- Canonical JSON unit representing a capability, grammar pack, or reusable structured component inside a UMG repository.

### CantoCore
- Rules/grammar or executable-logic surface associated with block behavior rather than passive memory representation.

### CyentCore
- Memory-card or representational layer that stores reusable descriptive or utility memory without directly executing code.

### ledger
- Provenance and audit structure attached to a block or memory card.

### schema_version
- Version field used to prevent drift and support reconciliation between repository data and validation expectations.

### merge_logic
- Deterministic deduplication and reconciliation structure used when merging or updating structured items; field validity and placement remain unresolved in this batch.

## Role / Structure Language

### MetaMolt / MOLT
- Referenced here as an evolution or mutation system for block transformation and refinement, not as a formal role-taxonomy change packet.

### content must be array
- Candidate structural rule indicating that `content` should use array form rather than string form in canonical block structure.

### unexpected field
- Any field present in repository data but not allowed by the active schema, such as `color` or possibly `merge_logic` depending on policy.

## Governance / Audit Language

### schema drift
- Divergence between the intended validation schema and the actual structure of repository blocks.

### pre-migration check
- Validation or audit step run before repository-wide migration or schema updates.

### observational scanner
- Non-mutating validator/reporting tool that inspects repository content without changing files.

## Runtime / Tooling Language

### Ajv validator
- JSON-schema validation surface used to compile schemas and check repository blocks.

### loose checker
- Secondary audit script using more permissive heuristics to identify likely structure problems before or alongside strict schema validation.

### pre-commit hook
- Repository control gate that enforces validation before changes are committed.
