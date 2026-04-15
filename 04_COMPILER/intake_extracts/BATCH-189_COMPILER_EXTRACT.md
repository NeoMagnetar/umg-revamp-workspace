# BATCH-189 - Compiler Extract

## Scope
Compiler- and implementation-facing implications extracted from the public-canon reconciliation source.

## High-Value Compiler Claims
1. Public compiler framing preserved in the source:
   - compiles Sleeve JSON
   - outputs RuntimeSpec and Trace
   - deterministic
   - headless
   - no model calls
   - structural compilation only

2. Public release details preserved:
   - v0.1.0
   - January 15, 2026
   - commit a8def80

3. The source identifies strong next-step compiler tasks:
   - publish machine-readable schemas for Sleeve, TriggerState, RuntimeSpec, Trace, Block, Bundle, MergeOperation, GovernanceRule
   - publish conformance matrix
   - clarify activation mapping from legacy runtime_behavior_flags.is_active to current TriggerState/synthesis flow
   - add explicit legacy Merge-as-role to merge-as-operation migration guidance

## Likely Compiler Audit Targets
- schema publication
- conformance reporting
- activation semantics mapping
- merge migration documentation
- role vocabulary normalization
- README/spec/tooling alignment
