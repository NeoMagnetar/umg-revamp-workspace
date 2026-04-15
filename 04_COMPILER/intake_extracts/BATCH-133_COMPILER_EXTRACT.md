# BATCH-133 — Compiler Extract

## Scope
Compiler-facing implementation and integration implications extracted from the source.

## High-Value Compiler Claims
1. `compileSleeve(sleeve, triggerState)` is the central compile surface and already returns runtime, trace, and error state.
2. Runtime and Trace are explicitly separate artifacts.
3. `MOLT_ORDER` is fixed in code as trigger, directive, instruction, subject, primary, philosophy, blueprint.
4. Priority behavior is concretely implemented and tested:
   - Override beats Explicit
   - lower `priorityOrder` wins within group
   - ambiguous peers without order can fail with `ERR_PRIORITY_AMBIGUOUS`
   - id tie-break resolves equal peers
   - missing `priorityGroup` defaults to Default
5. Bundles support `ranked` and `alternates` semantics with contract checks enforcing active-selection behavior.
6. Merges use explicit result blocks and optional cross-MOLT result typing.
7. Governance is typed through bindings, rules, conditions, target filters, and effects.
8. Forbidden and off blocks are removed from live runtime.
9. Required-versus-forbidden contradictions fail compilation.
10. NeoBlocks and NeoStacks are explicit runtime artifacts.
11. PromptSpec is derived after runtime selection rather than replacing runtime structure.
12. Contract checks assert prompt/runtime alignment, forbidden-block absence, primary selection, and tag-index invariants.
13. LangChain integration can plausibly sit around the existing compiler core without rewriting it.

## Likely Compiler Audit Targets
Role vocabulary mismatch against canon.
Governance effect enforcement coverage for override_priority and limit.
Bundle semantics documentation and code parity.
PromptSpec / RuntimePromptSpec contract status.
Tag normalization and reversibility guarantees.
LangChain Runnable boundary around `compileSleeve`.

## Risk Surface
Any integration that pushes execution logic into the compiler core would conflict with this batch.
Any documentation that hides tested priority behavior or bundle alternates/ranked semantics would underuse strong evidence present here.
Any assumption that current code vocabulary already equals canon vocabulary would be unsafe.
