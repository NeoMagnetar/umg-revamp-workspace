# BATCH-106_DEFINITIONS

## Scope Note
These definitions are extracted from a derived source summary. They are evidence candidates, not canon.

## Terminology Extract

### .block.json
- JSON file unit representing a reusable UMG block whose organization and validation depend on declared internal metadata.

### category
- Metadata field used to determine top-level block placement inside the repository hierarchy.

### molt_type
- Metadata field used to determine subtype/subfolder placement beneath category in the block repository hierarchy.

### Category → MoltType
- Implied canonical organization rule for routing blocks into `data/blocks/<Category>/<MoltType>/`.

### Misc / Unknown
- Fallback placement bucket used when metadata is missing, invalid, or unrecognized during reorganization.

### validation step
- Post-transform audit layer that checks whether reorganized blocks still conform to expected schema/type rules.

### dry-run
- Non-destructive planning phase that previews intended block routing before execution.

### reorg script
- Tooling surface that reads block metadata, computes target locations, and rebuilds repository structure.

## Composition / Schema Language

### content must be array
- Candidate structural rule inferred from validation failures indicating that canonical block `content` should be array-shaped rather than string-shaped.

### additional properties are not allowed
- Schema-enforcement condition indicating that fields such as `merge_logic`, `color`, or `export_config` may be disallowed unless explicitly defined.

### metadata-driven placement
- Principle that block location is derived from declared metadata rather than filename or existing path.

## Governance / Release Language

### push protection
- External repository enforcement layer that blocks pushes containing exposed secrets.

### history rewrite
- Destructive repository cleanup process used to remove secrets or invalid history before force-pushing a clean state.

### reorg-complete tag
- Release-like checkpoint indicating a stable repository state after reorganization and cleanup.

## Tooling / Workflow Language

### normalize before route
- Candidate compiler/reorg principle that metadata should be cleaned and canonicalized before filesystem placement is calculated.

### plan → execute → validate → commit
- Candidate canonical workflow for large block repository transformations.
