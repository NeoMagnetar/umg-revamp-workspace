# BATCH-020 — Private Resleever Homebase Review

## Batch Overview
This batch reviews a chat that translated abstract UMG ideas into a concrete OpenClaw/GitHub workflow centered on one private homebase repo: `UMG_ENVOY_Resleever`. It is strongest where it narrows scope, separates source assets from compiled outputs and active runtime state, and turns a UMG-oriented repo into a live workspace skill.

## Source Snapshot
- Source type: extracted chat summary
- Main focus: single-agent-first deployment, OpenClaw workspace skill setup, private GitHub homebase, runtime asset separation
- Evidence status: evidence only, not canon
- Maturity note: governance and broader public-library doctrine are intentionally deferred in favor of stabilizing one agent first

## Chat-Level Summary
The chat began with a broad launcher/homebase idea and then deliberately reduced scope to a smaller, more practical private repo. The result was `UMG_ENVOY_Resleever`: a one-agent homebase intended to store sleeves, MOLT blocks, NeoBlocks, NeoStacks, compiler assets, and explicit runtime state. The conversation then moved into concrete operational steps for OpenClaw setup, repo cloning into the workspace skills folder, skill discovery, repo scaffolding, and first control-file drafts.

The batch repeatedly preserves a useful runtime separation:
- source assets
- compiled outputs
- active runtime state

It also contributes a strong deployment order:
- stabilize one agent first
- keep the repo private
- make compiler integration explicit but phased
- expand later into a broader public UMG block/skill ecosystem only after the single-agent base is stable

## UMG-Relevant Extraction

### 1. Single-agent-first staging
- One private agent is the near-term target.
- `UMG_ENVOY_Resleever` is the chosen homebase identity.
- Public launcher / multi-agent ambition is deferred, not abandoned.
- Practical stabilization outranks ecosystem breadth.

### 2. Repo as homebase runtime surface
The repo is meant to hold:
- sleeves
- MOLT blocks
- NeoBlocks
- NeoStacks
- compiler assets
- active runtime state
- traces / compile output

### 3. Runtime separation rule
The strongest operational distinction in the batch is:
- keep source assets separate from compiled outputs
- keep compiled outputs separate from active runtime state
- avoid destructive overwrite patterns when practical
- preserve prior active artifacts where feasible

### 4. OpenClaw integration workflow
The repo becomes both:
- a private GitHub repo
- a live local OpenClaw workspace skill

Daily loop signaled by the batch:
- GitHub repo as source of truth
- local clone in `~/.openclaw/workspace/skills/UMG_Envoy_Resleever`
- OpenClaw loads the repo as a workspace skill
- commits/pushes keep GitHub and local skill in sync

### 5. Compiler-aware but phased
Compiler integration is necessary, but the batch explicitly splits it away from repo bootstrap.
Compiler-aware directories and scripts are expected from the start, but deeper compiler upgrades are deferred into later phases.

## Independent Review
This batch is valuable because it forces UMG into an operational substrate instead of leaving it as theory. The strongest contribution is not a new semantic doctrine; it is the staging discipline:
- smaller correct repo over speculative ecosystem
- explicit file classes
- explicit runtime control files
- explicit workspace-skill installation pattern

The conversation also improves project discipline by treating repo files as authoritative surfaces and by refusing to collapse sleeve, compiler, runtime-spec, and skill-wrapper concerns into one amorphous bundle.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**: asset class separation, sleeve/runtime/source distinctions
- **PHASE_2_COMPILER_IMPACT**: compiler-aware scaffold, compile-output/traces paths, active sleeve/stack runtime files
- **PHASE_3_DOCUMENTATION_IMPACT**: repo docs, scope docs, validation docs, source-of-truth language
- **PHASE_4_SKILL_ALIGNMENT**: OpenClaw workspace-skill behavior contract and metadata/frontmatter pattern
- **PHASE_5_PRD_AND_STAGING**: explicit two-stage rollout: private resleever first, public library later

## Action Outcome
- Accept as evidence for deployment sequencing and repo architecture.
- Do not treat the broader launcher/homebase concept as current canon.
- Preserve the private single-agent resleever path as the operative result of this batch.
- Use the batch as a staging input for compiler/runtime file layout, workspace-skill rules, and homebase repo documentation.

## Recommended Next Decision
Lock the private-homebase repo contract:
- required directories
- source-vs-compiled-vs-runtime boundaries
- active runtime control files
- skill metadata expectations
- compiler integration phase boundary
