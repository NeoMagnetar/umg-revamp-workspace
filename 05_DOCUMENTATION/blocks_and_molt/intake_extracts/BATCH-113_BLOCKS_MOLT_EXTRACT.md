# BATCH-113 — Blocks and MOLT Extract

## Block/sleeve/archive signal in this batch
- Blocks and NeoBlocks are archive targets from the start.
- Sleeves, sleeve styles, and sleeve formats are archive targets as well.
- The batch treats block and sleeve material primarily as something to serialize, compare, diff, and conflict-check.

## Proposed block payload structure
A typed `block` payload was proposed with:
- `block_id`
- `block_type`
- `text`
- `tags`
- `constraints`
- `lineage`

### Lineage pressure
Lineage fields were designed to preserve:
- source blocks
- merge method
- prior history

This makes archive use compatible with later merge/synthesis investigation.

## Proposed sleeve payload structure
A typed `sleeve` payload was proposed with:
- `sleeve_id`
- description
- governance reference
- lens
- priority
- tags
- stacks
- blocks
- optional JSON snapshot

## MOLT-role serialization signal
The chat does not revise MOLT semantics directly. It mainly pressures the project to ensure that MOLT-like roles are preserved as typed fields or typed payloads rather than left as unstructured prose.

## Structural tension surfaced
- Trigger, priority, merge, and bundle are named as extraction targets.
- Their deeper semantics are not developed here.
- The archive therefore stores representational placeholders for later synthesis rather than closing those doctrines in this batch.

## Candidate follow-up questions
- Should archive payloads use UMG-native field names or neutral archive-native names?
- How should MOLT-role-bearing artifacts be normalized across chats?
- What minimum lineage is required for merge-related artifacts?
- Are sleeves archived as snapshots, references, or both?
