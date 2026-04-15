# BATCH-180 — Compiler Extract

## Scope
Compiler- and importer-facing implications extracted from the deployment-workflow source.

## High-Value Compiler Claims
1. The current importer expects a JSON array of block objects.
2. Each block object must contain valid keys and a valid `molt_type`.
3. The unpack script writes output into `data/blocks/<molt_type>/`.
4. File naming is derived from `block_id` through a safe-filename routine.
5. Existing output files may be skipped instead of overwritten.
6. Malformed structures can produce errors such as:
   - `string indices must be integers, not 'str'`
7. Production-quality export should therefore validate:
   - file shape
   - object shape
   - required keys
   - valid `molt_type`
   - expected block count
   - surfaced exact filename

## Likely Compiler Audit Targets
Formal artifact-contract validation.
Grouped-bundle linting before unpack.
Count preview and mismatch detection.
Filename canonicalization.
Row-versus-category generation mode declaration.
Importer diagnostics and clearer failure messages.

## Risk Surface
Any generation workflow that allows silent format drift will continue to break downstream unpacking.
Any compiler/import design that ignores exact filename and count validation will miss one of the most practically important signals in this batch.
