# BATCH-179 — Three-Sleeve Poe Refactor and Repo Migration Review

## Batch Overview
Batch ID: BATCH-179  
Source Type: derived summary / repo migration, sleeve separation, and bounded envoy workflow consolidation  
Working Topic: three-sleeve Poe architecture, repo analysis/export/refactor stages, bounded envoys, fresh-repo seeding, staged alignment workflow  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source focuses on restructuring the `neo-umg-mcp-server` project around a three-sleeve Poe architecture and deciding whether to repair the current repo or rebuild from a cleaner baseline.
The strongest recurring themes are:
- explicit sleeve separation for Poe
- analysis before mutation
- export/package stage before rebuild
- bounded envoys with distinct roles
- terminal seat versus browser/GitHub seat separation
- branch/PR-based mutation rather than direct main-branch surgery
- leaning toward a fresh curated repo rather than risky in-place repair

This batch is especially valuable because it treats the repo itself as a modular system that should be scanned, documented, exported, and rebuilt through agent-usable stages.

## Chat-Level Summary
This batch is strongest as a practical migration-and-rebuild architecture.
Its central contribution is not new abstract UMG semantics, but a strong execution pattern:
understand first,
package second,
rebuild third,
align fourth.

The strongest reusable signal is the sleeve-aware repo workflow:
- CLI sleeve
- web sleeve
- assistant sleeve

The second strongest contribution is the envoy workflow:
- Repo-Insight Envoy
- Repo-Exporter Envoy
- Merge-Refactor Envoy

The third strongest contribution is the fresh-repo bias.
Rather than blindly merging local drift, tarball refactors, and current repo entropy, the source increasingly favors building a cleaner new repo from curated exports and then applying bounded alignment passes.

## UMG-Relevant Extraction

### Core UMG Semantics
- The repo is treated as a modular system to be scanned, decomposed, cleaned, exported, and rebuilt in stages.
- Clean alignment is prioritized over ad hoc repair.
- Context-first cognition is explicit: the agent should know the repo deeply before making mutations.

### MOLT Roles / Taxonomy
The source does not explicitly map these roles to formal MOLT names, but it strongly separates functional roles:
- read/analyze role
- export/package role
- mutate/refactor role
- browser/GitHub role
- terminal/dev role

Envoys behave like tightly scoped role wrappers.

### Merge
Merge is treated as risky and bounded.
The chat identifies merge-risk zones including:
- duplicate helpers
- duplicate servers
- mismatched endpoints
- outdated scripts
- local unpushed drift versus GitHub state
- tarball state versus live repo state

The preferred mechanism is PR-mediated reconciliation via a Merge-Refactor Envoy, not direct mutation of `main`.

### Bundle
Tarballs are treated as modular bundles.
Later refinement proposes generating a curated package such as `dist/pkg.tar.gz` from trusted files after a deep analysis pass.
Bundle logic becomes:
analyze → export curated package → seed new repo → align/refactor.

### NeoStack Architecture
The repo workflow itself behaves like a layered transformation stack:
- scan/analyze
- export/package
- seed new repo
- refactor/align
- CI/PR/merge

The runtime, UI, helpers, scripts, and docs are treated as coordinated layers rather than isolated files.

### Sleeve Identity / Resleeving
This batch explicitly centers on a three-sleeve Poe architecture:
- `poeCliAgent.ts` as terminal sleeve
- `poeWebAgent.ts` as web sleeve
- `poeAssistantAgent.ts` as assistant/background sleeve

Rename from `poeRuntimeAgent.ts` to `poeCliAgent.ts` is a sleeve identity clarification.
The broader repo plan assumes explicit sleeve identity should be reflected in files, routes, scripts, and package structure.

### Governance / Control
- branch-based changes
- PR review
- dry-run modes
- build/CI checks
- tightly scoped envoys
- minimized direct human editing

Control is pushed into structured automation rather than manual surgery.

### Output Blueprint / Rendering Separation
Strong separation is maintained between:
- analysis outputs (`overview.yml`, `depgraph.yml`, `todo.yml`)
- code mutation outputs
- package outputs
- runtime outputs such as new repo state and PRs

Blueprint-first behavior is explicit:
plan the repo before rebuilding it.

### Compiler / Runtime Logic
The source treats repo tooling as a transformation pipeline:
- scan repo
- build index/docs
- rename files
- rewrite imports
- patch routes
- add scripts
- compile/test
- open PR

`scanRepo()` and `RepoIndex` are runtime-analysis substrates.
`ts-morph` codemods are favored over loose text replacement.
Terminal/dev and browser/GitHub seats operate as distinct execution contexts.

### Documentation / Spec Language
Machine- and human-readable artifacts proposed:
- `overview.yml`
- `depgraph.yml`
- `todo.yml`

These are not decorative docs; they are operational scaffolding for later envoys.

### Skill / Agent Workflow
Concrete multi-agent workflow:
- Repo-Insight Envoy: read-only analysis and documentation generation
- Repo-Exporter Envoy: curate and package trusted files
- Merge-Refactor Envoy: mutate codebase, run codemods, open PR

Execution seats:
- terminal seat for local filesystem and dev work
- browser/GitHub seat for PR review and web-side operations

### Safety / Bounded Agency
- dryRun=true
- branch creation before mutation
- PR-based review
- CI/build gates
- privilege separation by seat
- main branch protected until reviewed PR exists

## Independent Review
This batch has high Stage 1 value because it translates UMG-style modularity into a practical repo-migration strategy.
The strongest contribution is not any one rename or route patch.
It is the staged agent-usable workflow:
analysis first, mutation second.

The explicit three-sleeve architecture is also strong because it turns sleeve separation into a real file-and-runtime refactor target rather than just a conceptual distinction.

The fresh-repo strategy is valuable because it recognizes that accumulated repo drift may be better handled by curated reseeding than by in-place surgery.

Main cautions:
- fresh repo versus in-place refactor was not locked immediately
- exact keep/exclude rules for export were not finalized
- envoy implementation remains conceptually clear but not fully specified
- exact doc schemas for overview/depgraph/todo were still provisional
- migration boundaries and history preservation remain open

## Roadmap Mapping
Primary domain: sleeve-aware repo migration and bounded envoy workflow

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, canon candidates, and contradiction flags are justified because the source contains strong staged runtime/migration logic, explicit sleeve separation, bounded envoy workflow, and unresolved implementation boundaries.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. analysis-before-mutation as operational doctrine
2. three-sleeve Poe architecture as concrete repo target
3. fresh-repo versus in-place refactor policy
4. envoy contract boundaries and seat privileges
5. structured repo-doc artifacts as required migration scaffolding
