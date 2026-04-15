# BATCH-080_COMPILER_EXTRACT

## Scope
Compiler/runtime-adjacent material explicitly supported by the source.

## Strong Signals
- Proposed runtime flow: **Retrieve -> Inject -> Render**
- Retrieval occurs at generation time, not just in precompiled prompt text.
- Vector search is part of the implied execution path.
- Retrieved material is injected before final rendering.
- Philosophy and Instruction shape execution order and priority, not just output tone.

## Candidate Runtime Mapping
1. Parse active stack/loadout
2. Detect RAG-enabled mode from Primary / configuration
3. Resolve retrieval domain from Subject
4. Apply Instruction pipeline rules
5. Retrieve candidate sources/snippets
6. Inject selected material into active context
7. Render final output under Philosophy / Blueprint constraints

## Compiler Questions Raised
- Is RAG triggered by presence of a Primary module, by user request, or by explicit runtime configuration?
- Is dynamic retrieval part of Merge resolution or a separate pre-render step?
- How should conflicting retrieved sources be handled?
- How should token budgets and overflow be managed?
- Does retrieval happen before all merge resolution, or can retrieval-backed Merge units participate alongside static Merge units?

## Candidate Tasks
- Add runtime hook for retrieval-backed Merge processing.
- Add source ranking / conflict handling specification.
- Add retrieval configuration surface: top-k, source weighting, fallback behavior.
- Add inspectability layer showing retrieved inputs before render.
