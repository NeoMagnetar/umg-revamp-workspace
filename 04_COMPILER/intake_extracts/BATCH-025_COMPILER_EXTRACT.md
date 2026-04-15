# BATCH-025 Compiler Extract

## Compiler-Relevant Doctrines
- Activation does not erase precedence.
- Lower bundles must not nullify higher-order rules.
- Exceptions must be declared at or above the level of the rule they qualify.
- Bundle order is precedence order for same-type grouped blocks.

## Required Compiler/Runtime Behavior
1. Preserve the three-layer pattern:
   - top doctrine
   - middle route activation
   - lower operational execution
2. Enforce that routed/activated behavior remains bounded by upstream doctrine.
3. Prevent lower operational bundles from introducing undeclared exceptions.
4. Distinguish Bundle from Merge in validation and execution semantics.

## Candidate Compiler Tasks
- Add precedence enforcement so active lower bundles cannot silently override higher-order rules.
- Preserve bundle order as local same-type precedence.
- Add validation that exception language exists at the correct doctrinal layer.
- Preserve gate activation and route selection as runtime behavior, not as exception generators.

## Notes
This batch is stronger on doctrine than on implementation detail. It should guide compiler constraints, not be mistaken for completed compiler spec.
