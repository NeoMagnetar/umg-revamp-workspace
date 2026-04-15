# BATCH-195 - CSL, Compiler v0, and umg-core Repo Plan Review

## Batch Overview
Batch ID: BATCH-195
Source Type: derived summary / CSL lock, compiler v0 formalization, and repo migration consolidation
Working Topic: UMG as tech-agnostic CSL, compiler/runtime separation, vocabulary freeze, same-type structural merge, RuntimeSpec and Trace, repo cleanup and greenfield `umg-core`
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source moved from broad UMG clarification into a highly formalized CSL and compiler session.
It repeatedly separated canon from implementation, locked vocabulary before continuing, and pushed toward a clean implementation path instead of continuing inside the older concept-heavy repo.

The strongest recurring themes are:
- UMG locked as a tech-agnostic Cognitive Specification Layer
- deterministic compiler as the interpreter of UMG canon
- strict distinction among MOLT type, role, Thought Unit, MOLT Block, Module, Stack, Sleeve, RuntimeSpec, and Trace
- same-type-only structural merge with semantic synthesis moved into generation
- strict glossary and document-order discipline to stop drift
- fresh `umg-core` style repo path with docs, schemas, compiler modules, tests, and runner
- practical workflow guidance for chat-first file output, AGENTS.md, Replit, and reduced reliance on unreliable browser-agent tooling

This source is especially valuable because it binds semantics, compiler logic, repo structure, documentation order, migration strategy, and contributor workflow into one implementation-facing canon batch.

## Chat-Level Summary
This batch is strongest as a CSL/compiler-foundation and implementation-planning source.

Its central contribution is the CSL lock:
UMG specifies cognition, not execution.

Its second strongest contribution is the compiler v0 contract:
the compiler is deterministic, interprets Sleeve input, and must emit RuntimeSpec plus Trace.

Its third strongest contribution is drift control through vocabulary freezing:
the glossary, the canon outline, and the separation of helper-layer authoring constructs from compiler-level primitives all work together to keep meaning stable.

## UMG-Relevant Extraction

### Core UMG Semantics
UMG was explicitly locked as a tech-agnostic Cognitive Specification Layer.
The source repeatedly states that UMG:
- specifies cognition
- does not execute cognition
- defines what cognition should be
- produces abstract cognition contracts rather than running tools or generating text directly
- should remain modular, deterministic, inspectable, composable, and testable

The source also preserves strong explanatory framing such as:
- turning prompting into cognitive engineering
- separating thinking from execution
- merging structure first, meaning later

### MOLT Roles / Taxonomy
Canonical MOLT types settled in the source:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint
- Off

Authority order settled in the source:
- Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off

Roles were introduced as a distinct layer from MOLT type.
Canonical roles preserved:
- PrimaryShell
- MergeContributor
- BlueprintGuide
- Off

Critical locked distinction:
- MOLT Primary is not Role PrimaryShell

The source also introduces key layering terms:
- Thought Unit = raw semantic idea before typing
- MOLT Block = typed Thought Unit with role and metadata
- Module = human-facing container grouping multiple MOLT Blocks
- Stack = both compiler-operation language and organizational grouping language, with the dual use flagged for further cleanup

### Trigger
Trigger was positioned as highest authority.
Compiler v0 Trigger semantics were narrowed to actions only with no condition evaluation.

Allowed trigger actions settled in the source:
- enable_blocks
- disable_blocks
- set_directive_params
- request_tool
- set_merge_mode

Trigger may not:
- rewrite block content
- reorder hierarchy
- suppress Trace

Trigger is treated as modifying compilation state, not semantic content.

### Priority
Authority order is repeatedly emphasized as fixed and deterministic.
The source preserves:
- higher authority constrains lower authority
- lower authority may not override higher authority
- stable sorting and stable trace ordering are required
- hierarchy is both ordering and safety boundary

This batch is especially strong on separating precedence from generative synthesis.

### Merge
A major conceptual distinction is locked between:
- structural merge at compiler level
- semantic synthesis at generation level

Structural merge is restricted to same-type only in order to preserve hierarchy, determinism, and traceability.
Cross-type merge is rejected at compiler level and reinterpreted as semantic synthesis inside the PrimaryShell.

Same-type structural merge is explicitly allowed for examples like:
- Philosophy + Philosophy
- Instruction + Instruction
- Directive + Directive
- Blueprint + Blueprint

Merge eligibility in compiler logic is preserved as:
- same `molt_type`
- same non-empty `merge_key`

Merge policies settled in the source:
- strict
- append
- dedupe_append
- compose_fields (treated as strict in v0)
- prefer_higher_rank

Conflict behavior settled:
- dev mode: deterministic winner plus warning
- prod mode: compile error / compile_failed

Strong explanatory phrases preserved:
- The compiler merges blocks. The AI merges ideas.
- UMG merges structure first, meaning later.

### Bundle
Module appears as the human-facing bundle/container of multiple MOLT Blocks.
Composite Block / Macro appears as an authoring-layer convenience that expands into multiple MOLT Blocks before compilation.

This preserves a clear distinction:
- compiler understands flattened MOLT Blocks
- humans may author higher-level convenience containers

Examples like "always tells a dad joke" are explicitly treated as composite authoring convenience rather than one canonical compiler atom.

### NeoBlock Composition
NeoCube / NeoBlock language is discussed as internal metaphor or alias rather than primary canonical terminology.
The recommendation in the source is to keep external canonical terms boring and interoperable while allowing Neo* language as internal metaphor or alias.

This batch therefore supports canonical discipline first and branded/metaphoric aliases second.

### NeoStack Architecture
NeoStack / Stack is discussed as a grouped cognitive dimension such as:
- personality
- legal/compliance
- strategy

Examples preserved:
- clever / funny / charming / sparky as likely Philosophy blocks
- California import/export law / disclaimers as likely Instruction blocks
- persuasive / customer-first as likely Directive blocks

A stack is explicitly clarified as not being the PrimaryShell by default.
Strong candidate line preserved:
- Stacks organize thinking. PrimaryShell defines output.

### Sleeve Identity / Resleeving
Sleeve is defined as a complete cognitive loadout/specification containing:
- blocks
- modules/stacks
- snaps
- defaults

Sleeve is repeatedly treated as:
- agent-ready
- not executable
- distinct from Agent

Strong preserved language:
- A Sleeve is an agent-ready cognitive loadout.

No formal resleeving protocol is finalized, but sleeves are clearly treated as swappable cognitive loadouts.

### Governance / Control
Governance and drift control are central in this batch.
The source repeatedly emphasizes:
- glossary as practical authority
- fixed document outline
- no silent changes
- no redefining terms without versioning
- drift as a real violation issue

A naming hierarchy is preserved:
- UMG as CSL
- MOLT as grammar
- compiler as interpreter
- RuntimeSpec as abstract cognition contract
- Trace as audit artifact

Canon freeze and versioning ideas appear, though not fully finalized into a completed section.

### Output Blueprint / Rendering Separation
Blueprint is repeatedly treated as structural/stylistic guidance, not output content.
BlueprintGuide is defined as silent influence only.
Blueprint content remains only under RuntimeSpec `format.blueprint_texts`.

The source strongly separates:
- structural placement
- generative rendering

RuntimeSpec is described as execution-neutral and channelized across:
- strategy
- constraints
- context
- values
- format
- tool requests

### Compiler / Runtime Logic
The compiler is defined as a deterministic interpreter of the CSL, not UMG itself.
Compiler outputs settle as:
- RuntimeSpec
- Trace

Strong rule:
- No Trace = not UMG

RuntimeSpec is defined as an abstract cognition contract, not prompt text or execution.
Trace is defined as a mandatory audit artifact recording steps, decisions, and final active blocks.

Compiler pipeline preserved in approximate order:
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

PrimaryShell invariant:
- exactly one per Snap
- zero or more than one causes compile error

RuntimeSpec field semantics preserved:
- primary_shell_block_id
- active_blocks
- strategy.directive_params / directive_texts
- constraints
- context.subject_texts / primary_texts / primary_shell_text
- values
- format.blueprint_texts
- tool_requests
- errors / warnings

Trace event vocabulary preserved:
- OFF_REMOVAL
- SNAP_SELECTED
- STACK_RESOLVED
- TRIGGER_FIRED
- BLOCK_ENABLED / BLOCK_DISABLED
- DIRECTIVE_PARAMS_SET
- HIERARCHY_OVERRIDE
- MERGE_ATTEMPT / MERGE_SUCCESS / MERGE_CONFLICT
- VALIDATION_ERROR / WARNING

Determinism is preserved as same input yielding same output, with stable sort and deterministic winner resolution.

### Documentation / Spec Language
A fresh repo doc spine is proposed for `umg-core`.
Top-level docs requested/generated/planned include:
- README.md
- AGENTS.md
- docs/index.md
- docs/spec/UMG_CANON_MASTER.md
- optional supporting spec docs

A formal canon outline is preserved:
- Part I - Identity and Scope
- Part II - Core Grammar (CSL Layer)
- Part III - Structural Operations
- Part IV - Artifacts
- Part V - Determinism and Semantics
- Part VI - Compiler Interpretation
- Part VII - Governance
- Appendices

The source also preserves a broad glossary including:
- UMG
- CSL
- MOLT
- MOLT Type
- Thought Unit
- MOLT Block
- Role
- PrimaryShell
- MergeContributor
- BlueprintGuide
- Off
- Authority Order
- Snap
- Stack
- Merge
- Semantic Synthesis
- Directionality Law
- Module
- Stack (Organizational)
- Sleeve
- Compiler
- RuntimeSpec
- Trace
- Composite Block / Macro
- Agent
- Alias Terms such as NeoCube / NeoStack / NeoSleeve

### Skill / Agent Workflow
The source discusses frustration with Agent/browser mode and repeatedly concludes:
- do not rely on browser or computer mode for building the compiler
- use plain chat to output full files in text
- constrain coding agents through AGENTS.md
- use Replit only after structure stabilizes

A strong directive pattern is preserved:
- output every file fully in chat
- do not assume repo access

A practical workflow emerges:
- clean repo
- add docs/spec
- add kernel compiler
- add tests/fixtures
- add runner
- then use Replit or similar

### Safety / Bounded Agency
UMG is repeatedly kept outside execution.
Agent is defined as external to UMG.
Trigger tool requests are constrained to flags only, not execution.
Safety-preserving restrictions include:
- no silent overrides
- no trace suppression
- no cross-type structural merge
- no hidden execution in compiler
- BlueprintGuide kept silent
- Off blocks excluded from operations and outputs

### PRD / Staging / Release
The source contains a PRD-style outline for the compiler covering:
- purpose
- goals
- canon rules
- outputs
- operations
- validation
- determinism
- pipeline
- directories
- tests
- milestones
- definition of done

Milestone staging preserved:
- M0: skeleton compile loop
- M1: Snap + Off + Validation
- M2: Stack
- M3: Triggers
- M4: Merge
- M5: RuntimeSpec builder
- M6: Tests + fixtures
- M7: Schemas + optional schema validation

A clean repo split strategy is preserved:
- archive the old conceptual repo
- create a new implementation repo such as `umg-core`
- old repo remains historical concept/archive
- old README should point to the new active core repo

Replit-friendly staging is also preserved:
- Node + TypeScript repl
- paste folder structure
- run tests
- use runner script on sample fixtures

## Independent Review
This is one of the strongest compiler-foundation and repo-migration batches in the intake set.
Its value is not only in semantics, but in tying vocabulary control, compiler rules, repo hygiene, contributor workflow, and implementation staging together in one disciplined package.

The strongest contribution is the CSL lock.
The second strongest contribution is the deterministic compiler v0 contract.
The third strongest contribution is the combination of glossary discipline and greenfield `umg-core` migration planning.

Main cautions:
- Role is a newly formalized layer and still needs careful documentation to avoid conflict with older usage
- Stack remains overloaded between compiler operation and organizational grouping, despite significant clarification
- Module and Composite Block / Macro are useful but still partly helper-layer rather than fully canonized CSL terms
- old repo language such as Merge as a MOLT type conflicts with current canon and requires explicit migration cleanup
- governance/versioning content appeared but was not fully finalized

## Roadmap Mapping
Primary domain: CSL canon, compiler v0 formalization, glossary discipline, and `umg-core` migration

Roadmap phases touched:
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING
- PHASE_6_GITHUB_EXECUTION
- PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. Role as a fully documented canonical layer
2. final naming split for compiler Stack versus organizational Stack/Module
3. `umg-core` as the authoritative greenfield repo path
4. migration cleanup for old repo language, especially Merge-as-type
5. governance/versioning section completion once terminology is fully frozen
