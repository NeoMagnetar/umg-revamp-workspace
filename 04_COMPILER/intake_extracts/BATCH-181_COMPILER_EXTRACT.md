# BATCH-181 - Compiler Extract

## Scope
Compiler- and generator-facing implications extracted from the block-generator setup source.

## High-Value Compiler Claims
1. A future generator should read:
   - raw category/block-name text
   - YAML
   - plain text
   - source documents

2. The generator should infer block semantics and write full JSON blocks into role-aware paths such as data/blocks/{molt_type}/{category}/.

3. The canonical template should remain the fill target for all generated blocks.

4. cantocore, snap_config, merge_logic, and ledger should be preserved as meaningful fields, not decorative placeholders.

5. Generation at scale should move out of one-shot chat output into workflow/runtime tooling.

6. Repo automation should only perform commit-back after generation succeeds and a valid diff exists.
