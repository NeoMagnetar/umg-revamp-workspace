# BATCH-179 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived repo-migration and sleeve-architecture summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Workflow Terms
**Repo-Insight Envoy**  
Read-only analysis actor that scans the repo and emits structured documentation artifacts.

**Repo-Exporter Envoy**  
Packaging actor that exports trusted or green-lit files into a curated package for reuse or reseeding.

**Merge-Refactor Envoy**  
Mutation actor that rewrites imports, renames files, harmonizes routes/scripts, and opens PR-based changes.

**Terminal Seat**  
Execution context for filesystem, local dev, codemods, package generation, and other local/runtime tasks.

**Browser/GitHub Seat**  
Execution context for PR review, browser-side operations, and hosted repo interactions.

## Sleeve Terms
**CLI Sleeve**  
Poe sleeve responsible for terminal/dev behavior.

**Web Sleeve**  
Poe sleeve responsible for web/browser-facing behavior.

**Assistant Sleeve**  
Poe sleeve responsible for assistant/background orchestration behavior.

## Definitional Candidates
Analysis first, mutation second.  
Clean alignment over ad hoc repair.  
Fresh repo seeded from curated package, then aligned by envoy.  
Give the agent the repo context it needs before asking it to mutate code.
