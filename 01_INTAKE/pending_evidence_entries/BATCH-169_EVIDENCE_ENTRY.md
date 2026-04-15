# BATCH-169 — Evidence Entry

## Batch ID
`BATCH-169`

## Topic
UMG Block Metadata Builder

## Source Type
Pasted chat/source summary treated as direct evidence input. fileciteturn19file0

## Core Evidence Signal
This batch documents a shift from loose UMG concept handling toward explicit **block-native encoding**. A UMG block is treated here as a self-describing JSON unit that carries its own role, snap behavior, merge behavior, runtime flags, provenance, and optional module links. The source also records a builder implementation path and a repo cleanup path that would operationalize those assumptions. fileciteturn19file0

## Strongest Claims Preserved as Evidence
1. Blocks must encode snap/stack/merge logic directly, not rely on vague external interpretation.
2. Canonical MOLT-type blocks were enumerated as explicit JSON blueprints, with Merge introduced as an additional candidate/operator block.
3. The builder should expose both visual composition and raw JSON simultaneously.
4. Sleeves are concrete loadable runtime objects and active sleeve state should be centralized.
5. Repo-level cleanup and schema normalization are required before scale. fileciteturn19file0

## Reliability Notes
The source is strong on implementation intent and schema expectations, but not all details are stabilized:
- Some earlier assistant outputs were corrected by the user.
- Schema names changed during the conversation.
- Folder/path cleanup was mid-flight.
- Merge canon status remained open. fileciteturn19file0

## Duplicate / Overlap Risk
Likely overlaps with prior batches on:
- builder/runtime structure
- sleeve loading and active-state behavior
- block schema and ontology
- optional AI-assist builder surfaces

## Contradiction / Tension Notes
Preserve explicitly:
- `cantocore` vs `canto_overlay`
- `merge_logic` vs `merge_behavior`
- Deployment color inconsistency
- Merge as canonical role vs operator/candidate role
- inline-copyable artifacts preferred over zip-first delivery in the originating chat context. fileciteturn19file0

## Disposition
`ACCEPT_AS_EVIDENCE`
