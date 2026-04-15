# BATCH-195 - Compiler Extract

## Scope
Compiler- and implementation-facing implications extracted from the CSL/compiler-foundation source.

## High-Value Compiler Claims
1. The compiler is a deterministic interpreter of the CSL, not UMG itself.
2. Canonical outputs are:
   - RuntimeSpec
   - Trace
3. Strong rule:
   - No Trace means not UMG
4. Compiler pipeline preserved in the source:
   - parse sleeve
   - validate basics
   - choose snap
   - select snap blocks
   - remove Off blocks
   - resolve stacks
   - apply triggers
   - apply authority ordering / hierarchy
   - merge same-type groups
   - validate PrimaryShell exactly one
   - emit RuntimeSpec + Trace
5. Trigger v0 is actions-only and may not rewrite content or suppress trace.
6. Structural merge is same-type only with explicit merge key and dev/prod conflict behavior.
7. Milestones preserved:
   - M0 skeleton compile loop
   - M1 Snap + Off + Validation
   - M2 Stack
   - M3 Triggers
   - M4 Merge
   - M5 RuntimeSpec builder
   - M6 Tests + fixtures
   - M7 Schemas

## Likely Compiler Audit Targets
- Role documentation and enforcement
- exact Stack naming split
- PrimaryShell uniqueness validation
- Trace event taxonomy
- same-type merge legality and conflict handling
- greenfield `umg-core` implementation path
- Replit-friendly but canon-safe compiler structure
