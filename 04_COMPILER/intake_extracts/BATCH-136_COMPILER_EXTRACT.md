# BATCH-136 — Compiler Extract

## Scope
Compiler-facing schema and contract implications extracted from the source.

## High-Value Compiler Claims
1. A persisted block may need a stable JSON envelope including id, label, description, MOLT type, tags, and payload.
2. `cantocore` appears as a viable compact payload surface for rule-oriented blocks.
3. Example data can be attached without altering the block’s semantic role.
4. Ledger metadata suggests provenance and verification may need standardized compiler/storage treatment.
5. `merge_logic` suggests some authors may expect block-local interaction hints, which requires canon review.
6. Empty extension arrays imply a possible extensible artifact surface even when currently unused.
7. UI/display/snap metadata should likely be distinguished from semantic/compiler fields.

## Likely Compiler Audit Targets
Canonical block JSON field set.
Semantic versus renderer/storage field boundaries.
Payload typing for `cantocore`.
Ledger field standardization.
Whether block-level merge logic is allowed or should be relocated.
Persistence of editability declarations.

## Risk Surface
Any compiler contract that conflates display metadata with semantic law would conflict with the likely direction implied by broader project evidence.
Any canon decision that ignores raw practical block artifacts like this risks becoming too abstract to implement.
