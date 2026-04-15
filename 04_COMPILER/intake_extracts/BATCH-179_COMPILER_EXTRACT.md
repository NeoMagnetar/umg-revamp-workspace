# BATCH-179 — Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the repo-migration source.

## High-Value Compiler Claims
1. Repo transformation should behave like a staged pipeline:
   - scan
   - document/index
   - export curated package
   - seed new repo
   - refactor/align
   - compile/test
   - PR/merge
2. `scanRepo()` and `RepoIndex` function as runtime-analysis inputs.
3. `ts-morph` codemods are preferred over loose text edits.
4. Structured documentation artifacts such as `overview.yml`, `depgraph.yml`, and `todo.yml` should become operational inputs for later mutation agents.
5. Execution context must distinguish terminal/dev actions from browser/GitHub actions.
6. Dry-run, branch creation, CI gates, and PR review are part of the mutation contract.

## Likely Compiler Audit Targets
Repo scan artifact schema.
Curated package keep/exclude rules.
Seat-aware execution boundaries.
Codemod contract and rename/import rewrite logic.
Fresh-repo seeding workflow.
PR-mediated alignment pipeline.

## Risk Surface
Any rebuild strategy that skips the analysis/export stages would discard one of the strongest safety and quality signals in this batch.
Any system that collapses terminal and browser privileges into one undifferentiated agent seat would weaken bounded control.
