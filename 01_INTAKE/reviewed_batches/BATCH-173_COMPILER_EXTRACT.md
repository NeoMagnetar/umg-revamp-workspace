# BATCH-173 Compiler Extract

## Candidate Pipeline
- nCube JSON definition
- code generation into Mojo or other target snippets
- compile to CPU / GPU / WASM / alternate backend
- produce artifact bundle
- hash or pointer registration back to the block record

## Runtime Responsibilities
- graph-based scheduling
- fused or chained kernel execution
- bundle caching by hash
- sleeve-level engine selection
- governance-aware approval checks before activation

## Important Architectural Constraint
The batch repeatedly treats the runtime engine as **pluggable**:
- MAX / Mojo is proposed as strong path
- but the higher-level block schema should not depend on one execution backend

## Compiler / Runtime Pressure on UMG
This batch suggests the project will eventually need:
- chain-agnostic pointer format
- runtime-agnostic artifact format
- registration model for compiled artifacts
- clear publish pipeline semantics
- loader behavior for approved bundles

## Risk Notes
None of these are finalized. They are implementation directions extracted from the source, not approved compiler requirements.
