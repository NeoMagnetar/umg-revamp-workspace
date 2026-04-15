# BATCH-169 — Definitions Extract

## UMG block
Atomic unit of logic and metadata for the builder. In this batch, a block is expected to be a self-describing JSON object carrying role, snap behavior, merge behavior, runtime flags, provenance, and optional code modules. fileciteturn19file0

## canonical MOLT types
Explicit JSON blueprints named in this batch:
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Trigger
- Deployment
- Off
- Merge (candidate/operator-style addition) fileciteturn19file0

## snap behavior
Encoded compatibility/attachment behavior that helps blocks connect and compose.

## stack
Composed arrangement of blocks where vertical layering and logical hierarchy matter.

## merge behavior
Embedded block-level conflict/composition behavior. Later preferred over earlier `merge_logic` wording in this source.

## runtime_behavior_flags
Per-block runtime markers such as trigger/execution/activation hints.

## canto_overlay
Later preferred schema term replacing earlier inconsistent `cantocore` usage in this source.

## sleeve
Persona/runtime definition stored in sleeve JSON and loaded into active runtime state.

## active_state.json
Runtime memory file intended to hold the full active sleeve state.

## block root
`blocks/` as the proposed single canonical block root for the repo/builder structure.

## schema guide
Upgraded markdown artifact in this batch intended to document purpose, key fields, hierarchy, examples, color grammar, and directory conventions. fileciteturn19file0
