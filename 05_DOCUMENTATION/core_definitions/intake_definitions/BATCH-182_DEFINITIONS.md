# BATCH-182 - Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived Builder implementation summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Terms
UMG Builder
A JSON-based visual tool and interface built on top of the broader UMG framework.

Template Manifest
Builder-specific JSON file that maps MOLT types to ordered arrays of block IDs for stack auto-population.

Static Block Runtime
Implementation model in which Builder behavior is driven by static `.block.json` files, runtime matrices, and scripts rather than a database backend.

Meta Category
Builder/runtime extension category introduced for overlay or agent-context concepts such as agent context, plan role, AI overlay, persona reference, and template type.

## Runtime Terms
snapMatrix.json
Global Builder runtime rule map for snap compatibility.

mergeMatrix.json
Global Builder runtime rule map for merge compatibility.

autopopulate_stack.py
Utility that loads blocks, matches them by tags or cantocore, and builds ordered stacks.

validate_manifest_refs.py
Validation utility that checks manifest references against actual block files.

## Definitional Candidates
- UMG is the framework; UMG Builder is one JSON-based implementation surface built on top of it.
- Builder uses static JSON only; no backend or database is required for the current app.
- Manifest-driven plan selection auto-populates the Builder stack.
