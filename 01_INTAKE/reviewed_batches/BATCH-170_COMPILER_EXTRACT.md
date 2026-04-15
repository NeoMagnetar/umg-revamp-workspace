# BATCH-170 Compiler Extract

## Compiler / Runtime Signals
- Merge priority must be formalized as engine logic.
- Snap and merge metadata should be exposed consistently across all block types.
- Alignment and Privacy appear to sit above ordinary content merge.
- Routing, Execution Mode, and Merge should remain distinct runtime concerns.

## Specific compiler-facing tasks implied
1. Standardize merge metadata across block types.
2. Standardize snap metadata across block types.
3. Formalize conflict-resolution hierarchy.
4. Distinguish:
   - model routing
   - execution environment selection
   - aggregation / merge behavior
5. Treat policy layers as hard controls rather than ordinary content layers.

## Runtime Tensions Preserved
- earlier vs later merge-priority explanations differ
- Merge block versus merge engine is not cleanly resolved
- dormant/experimental blocks should not silently enter active runtime behavior

## Why this matters
Without a stable merge/snap contract, generic block compilation and runtime assembly will remain fragile.
