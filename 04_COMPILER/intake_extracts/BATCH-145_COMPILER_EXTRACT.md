# BATCH-145 — Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the metadata-policy source.

## High-Value Compiler Claims
1. Blocks should carry a structured metadata envelope including fields such as label, category, description, editable fields, MOLT type, tags, overlay, ledger, trigger, and export configuration.
2. Trigger metadata is formalized as an object with:
   - `type`
   - `action`
   - `conditions`
   - `next_block`
3. Trigger types currently surfaced include:
   - `on_click`
   - `on_submit`
   - `on_load`
   - `on_custom_event`
4. Snap/merge/fusion logic should support compatibility highlighting, merged field inheritance, and merge history retention.
5. Metadata should remain present in exports even when UI display chooses to hide or simplify it.
6. A View-MOLT inspector is a plausible runtime/developer surface for exposing block structure without burdening casual users.
7. Hackathon-scope implementation should remain practical and not depend on full Web3 infrastructure.

## Likely Compiler Audit Targets
Canonical metadata field set.
Trigger-object standardization.
View-MOLT inspector data source requirements.
Snap/merge lineage retention.
Export metadata preservation.
Boundary between rich schema and simplified generated files.

## Risk Surface
Any builder that hides MOLT structure so completely that blocks become semantically opaque would conflict with this batch’s strongest signal.
Any public build that depends on postponed Web3 layers would conflict with the staged scope captured here.
