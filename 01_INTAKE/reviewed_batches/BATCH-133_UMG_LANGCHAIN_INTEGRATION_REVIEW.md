# BATCH-133 — UMG LangChain Integration Review

## Batch Overview
Batch ID: BATCH-133  
Source Type: derived summary with implementation-surface exposure, not a raw transcript  
Working Topic: LangChain integration surface, compileSleeve contract, runtime artifacts, governance/tooling boundary, priority tests, tag indexes, contract validation  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation titled `UMG LangChain Integration`.
It summarizes a chat that began with product-direction discussion around LangChain as an execution harness for UMG and then exposed concrete TypeScript compiler files, tests, and typed runtime surfaces.
The batch includes implementation-facing details for `compileSleeve`, runtime outputs, trace behavior, governance handling, bundle/merge semantics, NeoBlock/NeoStack construction, tag indexing, prompt derivation, and contract checking.
Because the source is a derived summary rather than a raw transcript or direct file dump, it should be treated as strong evidence of current implementation direction and integration potential, but not as automatic canon.

## Chat-Level Summary
This batch is a high-value bridge between UMG theory and an agent-usable tooling surface.
Its central contribution is architectural clarity:
UMG remains the deterministic specification/compilation layer,
while LangChain is positioned as the execution harness around that layer.
Unlike purely conceptual integration talk, this batch also exposes concrete compiler-facing contracts already present in code:
typed runtime artifacts,
trace events,
priority resolution behavior,
bundle/merge handling,
NeoBlock/NeoStack construction,
prompt derivation,
and invariant checks.
That makes the batch valuable not only for product direction, but also for documentation, audit, and integration staging.

## UMG-Relevant Extraction
UMG is framed as deterministic brain-spec or specification layer, while LangChain is framed as runtime/execution harness.
`compileSleeve(sleeve, triggerState)` returns a `CompileResult` with `runtime?`, `trace`, and `hasErrors`.
Runtime output and Trace output are explicitly separated.
Runtime carries compiler metadata including `compilerVersion: "v0"` and `compiledAt`.
`MOLT_ORDER` is fixed in code as trigger, directive, instruction, subject, primary, philosophy, blueprint.
Code-defined `MoltType` matches that order.
Code-defined `BlockRole` includes `primary_shell`, `merge_contributor`, `annotation`, and `off`.
Priority surfaces are explicitly implemented through `priorityGroup` and `priorityOrder`.
The code comment states tier order `Override > Explicit > Default > Fallback`, with lower numeric `priorityOrder` winning within the same group.
Tests indicate:
Override beats Explicit,
lower order wins within same group,
ambiguous same-group peers without order fail with `ERR_PRIORITY_AMBIGUOUS`,
ties fall to alphabetical id winner,
and missing `priorityGroup` defaults to Default.
Bundle segments are explicitly modeled with intents `ranked` and `alternates`.
Merge segments are explicitly modeled with `resultBlockId`, optional `resultMoltType`, and an `allowAdvanced` reservation field.
`compileSleeve` applies merges before bundles and governance.
Bundles are recorded and emitted into runtime.
Governance is fully typed through bindings, rules, conditions, target filters, and effects.
Governance scopes supported in code are sleeve, stack, stacks, and block.
Governance targets can filter by MOLT types, block ids, stack ids, tags, and roles.
Governance effects include forbid, require, prefer, override_priority, and limit.
Forbidden and off blocks are excluded from live runtime.
Required/forbidden contradictions fail compilation.
`RuntimeNeoBlock` includes ordered block ids, by-MOLT organization, bundle ids, merge ids, selected primary, and active selections.
NeoBlocks are built after authority and per-type selection passes.
`RuntimeNeoStack` includes id, optional domain key, and NeoBlock ids.
Prompt output is separated through `PromptSpec` / `RuntimePromptSpec`.
Prompt sections are derived from runtime structure rather than collapsing runtime and render text together.
Runtime indexes include UI-friendly lookups such as titles, stack names, and normalized tag indexes.
Contract validation checks promptSpec/runtime alignment, forbidden-block absence, primary selection, and tag-index invariants.
The LangChain proposal keeps compiler core intact and suggests fitting a Runnable or governed execution layer around existing compile outputs.

## Independent Review
This batch has unusually high Stage 1 value because it combines two evidence classes that often drift apart:
integration vision and actual compiler contract.
The strongest contribution is that it provides a plausible way to make UMG agent-usable without dissolving the compiler into an agent framework.
The phrase-level architecture is clear:
UMG compiles,
LangChain runs.
That boundary aligns well with other strong evidence in the project about UMG as specification, compilation, and trace rather than execution.
The implementation details matter just as much.
Priority behavior, bundle alternates/ranked semantics, prompt derivation, runtime indexes, and contract checks are all concrete enough to inform audit and documentation work immediately.
Main caution: this batch also reveals some surface mismatches with broader canon direction, especially around role vocabulary (`annotation`), absence of some preferred role names, and the partially visible enforcement path for some governance effects.
Those should be preserved as tensions rather than flattened into assumed alignment.

## Roadmap Mapping
Primary domain: compiler integration surface and implementation-contract exposure

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: exposes canon-relevant tensions between current code vocabulary and preferred semantic vocabulary.
Phase 2: provides direct compiler-contract evidence for pipeline stages, priority rules, bundle/merge semantics, governance bindings, prompt derivation, and invariant checking.
Phase 3: offers documentation-ready material for exact compile flow, runtime artifacts, and tested behavior.
Phase 4: creates a plausible agent/tool integration surface without moving execution into the compiler core.
Phase 5: supports PRD input for a developer test bench and staged integration path.
Phase 6: suggests packaging and repo surfaces for integration tooling around existing compiler code.
Phase 7: strengthens the case for a publishable developer-facing runtime/testing surface.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the batch contains concrete compiler contracts, integration-facing product direction, and explicit vocabulary/runtime tensions that should remain visible.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. LangChain-around-compiler boundary
2. code vocabulary versus canon vocabulary alignment
3. documented priority and bundle behavior from tests
4. PromptSpec / RuntimePromptSpec contract status
5. governed-tools integration path
