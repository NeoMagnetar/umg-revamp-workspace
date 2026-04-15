# BATCH-201 — Compiler / Runtime Extract

## Scope
This extract captures runtime migration and toolchain implications from the repo cleanup.

## Source-Backed Points
- Canonical block unit is now one `.block.json` under `data/blocks/{MOLT_TYPE}/`.
- `consolidate_blocks.py` is used to convert aggregate dumps into canonical block files.
- `validate_blocks.py` is updated to validate only canonical block locations.
- `generate_manifests.py` regenerates manifests from the canonical block tree.
- `validate_manifest_refs.py` remains part of the intended validation flow.
- `report_structure.py` is updated to scan only `data/blocks`.
- Runtime path expectations are being normalized toward canonical directories.
- `poe_nl_agent.py` functions as an NL-to-task runtime layer for file ops, block generation/merge, envoy generation/run.

## Compiler / Runtime Pressure
This batch strongly pressures the project toward:
- canonical input tree enforcement
- lossless migration from legacy bundle dumps
- manifest generation as a derived artifact rather than a parallel source of truth
- clearer separation between runtime executors and structural/config files
- stronger validator coverage over canonical blocks and manifest refs

## Conservative Intake Reading
Useful for:
- repo/runtime cleanup
- canonical input normalization
- manifest generation workflow
- Poe helper execution surface planning

Not enough to:
- settle final semantic status of `Deployment` and `Merge`
- settle the final web-builder integration model for Poe
- settle every future runtime dependency
