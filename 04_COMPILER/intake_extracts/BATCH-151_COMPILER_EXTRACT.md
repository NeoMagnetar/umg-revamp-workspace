# BATCH-151 — Compiler Extract

## Scope
Compiler- and engine-facing implications extracted from the v3.0 schema source.

## High-Value Compiler Claims
1. Snap, Merge, and Stack are the core engine operations.
2. Runtime behavior flags include:
   - `render_injection_priority`
   - `is_primary_directive`
3. Merge priority hierarchy is:
   Trigger > Directive > Instruction > Subject > Primary > Merge > Philosophy > Blueprint > Off
4. Merge-related fields include:
   - `merge_as`
   - `merge_strategy`
   - `merge_origin`
5. Trigger blocks execute independently and do not inject prompt text.
6. Blocks can expose tools via `function_spec`.
7. `code_modules` provide multi-language execution planning across frontend, backend, and AI toolchain surfaces.
8. `mergeEngine.js` is a direct implementation candidate.

## Likely Compiler Audit Targets
Canonical merge semantics.
Single Primary versus mergeable Primary law.
Directive vs Instruction behavior split.
Snap config normalization.
Trigger execution model.
function_spec to tool-calling integration.
Migration from `code_injection` to `code_modules`.
