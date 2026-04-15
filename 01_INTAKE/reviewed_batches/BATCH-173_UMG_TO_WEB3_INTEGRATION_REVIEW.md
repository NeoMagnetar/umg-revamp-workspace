# BATCH-173 UMG to Web3 integration — Review

## Source Snapshot
This batch reviews a chat about mapping UMG into a Web3 ecosystem using low-cost chains, off-chain storage, and on-chain provenance. The source treats UMG blocks as publishable modular assets that can be minted, bundled, licensed, remixed, compiled, governed, and deployed while keeping heavy execution off-chain.

## Chat-Level Summary
The source proposes a Web3-facing deployment and commercialization model for UMG. The core pattern is consistent throughout the batch: keep identity, provenance, hashes, approvals, and lightweight governance on-chain; keep block JSON, binaries, compute, storage, and execution off-chain. It also proposes a compiler path from block JSON into Mojo/MAX or other runtime targets, plus marketplace and builder workflows for publish, license, remix, and bundle distribution.

## UMG-Relevant Extraction
The strongest UMG signal in this batch is not “crypto” in the abstract. It is the architectural separation between:
- identity / provenance / governance
- compiled artifacts / runtime execution / heavy storage

The source also materially extends the current structural vocabulary:
- nCube as atomic publishable block
- nStak as composable bundle / graph unit
- nSleeve as sovereign runtime wrapper
- Envoy as a governance-capable agent analogue

The batch proposes a practical publish path:
1. create/select a block in the builder
2. pin JSON or metadata off-chain
3. optionally compile the block
4. write hash/pointer/provenance on-chain
5. import approved bundles into a sleeve/runtime

## Independent Review
This is strong Stage 1 evidence for deployment architecture, marketplace direction, and provenance-aware runtime packaging. It is especially useful because it preserves a clean output-layer separation: blockchain is treated as bookkeeping, identity, governance, and history; execution remains off-chain. That pattern is directly relevant to UMG because it mirrors existing project pressure toward modular identity, pluggable runtime engines, and explicit artifact lineage.

However, the batch remains provisional in several ways:
- MAX/Mojo is presented as a strong path but explicitly optional.
- Marketplace rights, royalties, and licensing are not settled.
- Governance mechanisms are described directionally, not finalized.
- Web3 UX cost/complexity tradeoffs remain open.
- The on-chain / off-chain model is an implementation proposal, not a ratified canonical architecture.

## Roadmap Mapping
### Phase 1 — Core Alignment
Relevant for terminology around nCube / nStak / nSleeve / Envoy in deployment context.

### Phase 2 — Compiler Impact
Directly relevant to code generation, artifact hashing, bundle registration, and runtime-engine abstraction.

### Phase 3 — Documentation Impact
Relevant for public explanations of provenance, publish flow, builder integration, and chain/runtime separation.

### Phase 5 — PRD and Staging
Relevant for MVP scoping: provenance pointer + off-chain compile path first, marketplace/governance later.

### Phase 8 — Post-Release Expansion
Relevant for marketplace, licensing, creator economy, and no-code site generation ambitions.

## Action Outcome
Disposition: **ACCEPT_AS_EVIDENCE**

Reason: The batch gives the project a coherent Web3 and runtime-deployment direction while clearly stopping short of final architecture. It should inform later synthesis on compiler/runtime abstraction, publish flow, provenance, and marketplace design, but it should not be promoted to canon at Stage 1.
