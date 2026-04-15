# BATCH-187 - Compiler Extract

## Scope
Compiler- and implementation-facing implications extracted from the canon-formalization source.

## High-Value Compiler Claims
1. Compiler input/output contract is framed as:
   - input: Sleeve JSON
   - output: RuntimeSpec + Trace

2. Deterministic compiler pipeline:
   - parse sleeve
   - validate sleeve basic
   - choose snap
   - select snap blocks
   - remove Off
   - resolve stacks
   - apply triggers
   - enforce authority / directionality
   - merge same-type groups
   - validate PrimaryShell exactly one
   - emit RuntimeSpec
   - emit Trace

3. Trigger v0 is limited to state modification, not content rewriting or condition evaluation.

4. Stack resolution is same-type only and deterministic.

5. Merge is same-type only and keyed by same non-empty merge_key.

6. The compiler is the enforcing spine of UMG; without it, UMG remains inert specification.

## Likely Compiler Audit Targets
- CSL-to-compiler contract
- Trigger v0 legality
- PrimaryShell uniqueness
- RuntimeSpec field normalization
- Trace event taxonomy
- merge conflict dev/prod split
- fresh umg-core implementation path
