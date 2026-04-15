# BATCH-147 — Blocks and MOLT Extract

## Scope
Block- and MOLT-structure signals extracted from the generation-protocol source.

## Direct MOLT Signal
Every generated block in the described workflow used:
- `molt_type: "Primary"`

## Structural Meaning
This means the production pipeline treated the generated domain blocks as Primary-layer units by default.
The source does not justify whether this is a true semantic conclusion for each domain block or simply a workflow default.

## Block Shape Signal
The batch provides a concrete repeated block envelope including:
- identity fields
- descriptive fields
- tags
- ledger/provenance
- trigger slot
- export configuration

## Visibility Signal
The source states that block structure is intended to be visible through the MOLT Viewer / View JSON surface in the Citadel.

## Useful Example Signal
This batch is especially valuable because it shows how MOLT assignment and block schema behave at mass-production scale, not just in isolated examples.
