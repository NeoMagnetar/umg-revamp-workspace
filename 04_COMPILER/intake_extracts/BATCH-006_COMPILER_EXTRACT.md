# BATCH-006 — Compiler Extract
## Compiler-Relevant Signals
- The current compiler is described as primarily a normalization, layout, and indexing engine rather than a full authority resolver.
- A missing **Authority Resolution** phase is identified between normalization and prompt assembly.
- PromptSpec should eventually consume resolved active winners, not the full pre-resolved compiled set.
- Tags, signals, conditions, and resolved state should be distinguished in both data flow and output semantics.
- Governance should be enforced before prompt emission, especially for protected keys, illegal overrides, and safety tightening.
- Display metadata can improve editor/compiler usability without changing core semantics.

## Candidate Compiler Tasks
- Add Authority Resolution between normalization and prompt assembly.
- Emit `resolvedStates` per stack and/or runtime surface.
- Make promptSpec consume the resolved active set.
- Add runtime tag / signal / condition evaluation path.
- Support singular-role policy, alternates, exclusivity, and conditional winner selection.
- Add block metadata / display artifacts: `createdAt`, `updatedAt`, `createdSeq`, `displayKey`, `preview`, `laneIndex`, `inLaneRank`, `status`.
- Clarify trigger semantics so trigger blocks can become executable runtime selectors rather than prompt-only descriptors.

## Compiler Caution
This batch narrows the implementation gap well, but several items here remain candidate contract work. They should not be treated as already-implemented compiler behavior.
