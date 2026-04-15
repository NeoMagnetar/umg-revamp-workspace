# BATCH-187 - CSL Canon, Compiler, and umg-core Migration Review

## Batch Overview
Batch ID: BATCH-187
Source Type: derived summary / canon formalization, compiler planning, and repo migration consolidation
Working Topic: UMG as CSL, canonical documentation structure, deterministic compiler, glossary authority, domain versus stack clarification, fresh umg-core repo path
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source captures a major canon-forming session that moved UMG from loose conceptual framing into a structured canonical system with bounded scope, locked vocabulary, ordered documentation, and a deterministic compiler model.

The strongest recurring themes are:
- UMG locked as a tech-agnostic Cognitive Specification Layer
- MOLT as the formal grammar of UMG
- deterministic compiler with RuntimeSpec and Trace as required outputs
- strict separation among block, stack, snap, domain, sleeve, compiler, RuntimeSpec, and Trace
- glossary authority and anti-drift governance
- fresh repo strategy centered on umg-core
- archival treatment for the older concept repo

This source is especially valuable because it ties semantics, documentation, compiler behavior, governance, and migration strategy together in one coherent batch.

## Chat-Level Summary
This batch is strongest as a canon-foundation and compiler-foundation source.

Its central contribution is the CSL lock:
UMG specifies cognition rather than executing it.

Its second strongest contribution is the deterministic compiler contract:
the compiler is the enforcing interpreter of UMG canon and must emit RuntimeSpec plus Trace.

Its third strongest contribution is anti-drift governance:
the glossary is treated as language authority, documentation order is fixed, and extensions are explicitly isolated outside canon.

## UMG-Relevant Extraction

### Core UMG Semantics
UMG was locked as a tech-agnostic Cognitive Specification Layer.
UMG was explicitly separated from:
- model execution
- agent loops
- orchestration
- runtime logic
- tool execution
- prompt engineering

UMG was repeatedly described as:
- modular
- deterministic
- inspectable
- composable
- traceable

MOLT was positioned as the formal grammar of UMG.
RuntimeSpec was defined as an abstract cognition contract.
Trace was defined as the mandatory audit artifact.
A strong compliance principle in the source:
- no Trace means not UMG-compliant

### MOLT Roles / Taxonomy
Canonical MOLT types were locked as:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint
- Off

Authority order was locked as:
- Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off

Roles were separated from MOLT types and locked as:
- PrimaryShell
- MergeContributor
- BlueprintGuide
- Off

PrimaryShell was defined as the single output anchor per snap.
PrimaryShell was explicitly stated not to be the same thing as MOLT Primary.

### Trigger
Trigger was defined as the highest-authority block type.
Trigger v0 actions were limited to:
- enable_blocks
- disable_blocks
- set_directive_params
- request_tool
- set_merge_mode

Trigger was explicitly prohibited from:
- rewriting Primary
- rewriting Instructions
- reordering hierarchy
- suppressing Trace
- evaluating conditions in v0

Tool requests were defined as external signals only, not execution.

### Priority
Authority was defined as cognitive constraint power, not visibility or UI position.
Directionality law was locked as influence flowing inward toward the PrimaryShell.
Lower-authority blocks were stated to never override higher-authority blocks.
Stacking was clarified as same-type-only resolution using stack_key and stack_rank.
MOLT authority order was fixed and non-configurable.

### Merge
Merge was redefined as an operation, not a MOLT type.
Merge was restricted to:
- same MOLT type
- same non-empty merge_key
- compatibility checks

Merge policies locked for v0:
- strict
- append
- dedupe_append
- compose_fields (treated as strict in v0)
- prefer_higher_rank

Merge conflict handling was defined as:
- dev mode: deterministic winner plus warning plus trace
- prod mode: compile failure plus trace

Merge was repeatedly distinguished from stack:
- stack chooses
- merge combines

### Bundle
The source treated personality-like or domain-like groupings as compositions rather than compiler primitives.
UI-level collapsing of multiple blocks into a visible bundle was treated as a visualization convenience rather than logical merge.
Bundle-like concepts were treated as human-facing groupings, not canonical compiler objects.

### NeoBlock Composition
A block was locked as a singular atomic unit of cognition.
A block was clarified as:
- one idea
- one rule
- one value
- one constraint
- one framing decision

Blocks were described as inert, declarative, and lifeless until composed and compiled.
A block was explicitly distinguished from:
- domain
- stack
- snap
- sleeve

Human-authored and system-authored blocks were both allowed.
Changed meaning should create a new block rather than silently mutating an old one.

### NeoStack Architecture
Stack was canonically locked as a mechanical same-type priority resolution system.
The user's broader intuitive use of "stack" for personality, morality, skillsets, or customer service was examined and separated from compiler meaning.
Domain emerged as the leading human-facing term for grouped behavior or concern areas.
The source repeatedly emphasizes:
- stacks do not create context
- stacks resolve conflict within a type

### Sleeve Identity / Resleeving
Sleeve was defined as the highest-level container of potential cognition.
A sleeve contains:
- blocks
- domains
- snaps
- defaults
- metadata

Sleeve was described as lifeless by design.
A sleeve was explicitly distinguished from an agent and from runtime state.
Old blocks should be preserved, disabled, or replaced through versioning rather than silently mutated.

### Governance / Control
Canon governance became a major theme.
The source locked:
- canonical documentation structure
- sequencing order
- glossary authority
- versioning and governance language
- drift prevention rules

Explicit anti-drift rules included:
- no casual redefinition
- no silent synonym drift
- no UI-driven reinterpretation of canon

Extensions were isolated into a non-canon section to protect core meaning.
The source repeatedly emphasizes that if something violates canon, it is not UMG.

### Output Blueprint / Rendering Separation
Blueprint was repeatedly separated from Primary, Instruction, and Philosophy.
Blueprint was locked as format / structure / style influence only.
BlueprintGuide was defined to ensure blueprint remains silent and is not emitted as direct content.
RuntimeSpec preserves blueprint information under format rather than constraints or values.

### Compiler / Runtime Logic
The compiler was formalized as a deterministic interpreter of the UMG CSL.

Compiler pipeline locked in order:
- parse sleeve
- validate sleeve basic
- choose snap
- select snap blocks
- remove Off blocks
- resolve stacks
- apply triggers
- enforce authority / directionality
- merge same-type groups
- validate PrimaryShell exactly one
- emit RuntimeSpec
- emit Trace

RuntimeSpec was locked as structured, execution-neutral output rather than a prompt.
Trace was locked as mandatory, deterministic, canonical, and audit-oriented.

RuntimeSpec fields discussed in detail:
- strategy
- constraints
- context
- values
- format
- tool_requests
- active_blocks
- errors
- warnings

### Documentation / Spec Language
The source produced a full canonical documentation structure:
- 0.1 README
- 0.2 QUICKSTART
- 1.1 WHITE_PAPER
- 1.2 UMG AS A COGNITIVE SPECIFICATION LAYER
- 2.1 GLOSSARY
- 3.1 MOLT_OVERVIEW
- 3.2 MOLT_TYPES
- 3.3 AUTHORITY_AND_DIRECTIONALITY
- 4.1 BLOCKS
- 4.2 DOMAINS
- 4.3 SNAP_AND_SCOPE
- 5.1 STACKING
- 5.2 MERGE
- 6.1 SLEEVE
- 6.2 COMPILER
- 6.3 RUNTIMESPEC
- 6.4 TRACE
- 7.1 VERSIONING
- 7.2 CANON_GOVERNANCE
- 8.1 EXAMPLES
- 8.2 UMG VS OTHER SYSTEMS
- 9.1 EXTENSIONS

The source repeatedly reinforced that this plan and order are fixed and should not be skipped.

### Skill / Agent Workflow
The source explicitly found agent/browser mode unreliable for this use case.
Plain chat text output became the preferred workflow.
Agent-ready compiler prompts were produced and tightened into greenfield directives.
AGENTS.md was introduced as a repo guardrail for coding agents.
The old repo was assessed as conceptually rich but structurally incomplete for compiler work.

### Safety / Bounded Agency
UMG was repeatedly bounded away from acting as:
- an agent
- a tool executor
- a runtime
- a memory system

Trigger actions were bounded tightly.
Extensions were isolated from canon.
Trace, compiler enforcement, and determinism were positioned as safeguards against hidden behavior and silent drift.

### PRD / Staging / Release
A PRD-style compiler outline and implementation plan were created.
A fresh repo blueprint was defined:
- umg-core
- docs/
- kernel/
- schema/
- compiler/
- tests/
- scripts/
- examples/

The old GitHub repo was recommended for archive and preservation while a fresh repo is created for the actual compiler core.
The source suggests sequencing:
- lock glossary
- lock white paper
- lock mechanics
- lock compiler spec
- then build

## Independent Review
This is one of the strongest canon-foundation batches in the intake set.
Its value is not only in definitions, but in binding terminology, compiler behavior, governance process, and migration strategy into one disciplined framework.

The strongest contribution is the CSL lock.
The second strongest contribution is the deterministic compiler contract.
The third strongest contribution is anti-drift governance backed by ordered documentation and glossary authority.

Main cautions:
- domain was strongly favored as the human-facing grouping term, but still stress-tested
- UI and graph mechanics remained concept-level rather than final canonical spec
- some explanatory phrases introduced during discussion may not all be desired as final canon vocabulary
- nested snap visualization remained conceptual rather than fully encoded behavior

## Roadmap Mapping
Primary domain: canon semantics, compiler contract, governance discipline, and umg-core migration

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
1. CSL language as top-level identity canon
2. domain as the final human-facing grouping term or not
3. compiler v0 contract as formal implementation law
4. glossary/document-order governance as canon process law
5. archive strategy for the old repo versus activation of fresh umg-core
