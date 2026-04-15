# BATCH-165 Compiler / Runtime Extract

## Runtime Model Captured by Source
The source implies a concrete builder runtime sequence:

1. user selects a plan
2. manifest is loaded
3. manifest provides block IDs
4. individual block definitions are fetched/parsed
5. valid blocks populate active state
6. canvas and graph renderer consume active state

## Runtime Failure Classes Named or Implied
- missing block file
- failed fetch
- non-JSON content-type
- duplicate block IDs
- invalid edge source/target
- zero-height graph container
- stale state/local storage interference
- import/alias resolution failures

## Candidate Runtime Hardening Tasks
- throw explicit errors when a block path fails
- require `response.ok`
- require JSON content-type
- reject duplicate IDs
- reject unknown edge endpoints
- wrap graph in `ErrorBoundary`
- add deterministic layout
- add validation npm script
- ensure fit/zoom defaults expose graph immediately

## Candidate Compiler/Audit Tasks
- corpus validator for block JSON integrity
- aggregated `blocks.json` generation if downstream tooling needs it
- deterministic auto-layout pass for graph visualization
- CI checks for duplicate IDs and invalid edges

## Evidence Status
This material is implementation evidence, not canonical compiler law. It is most useful for audit and staging queues.
