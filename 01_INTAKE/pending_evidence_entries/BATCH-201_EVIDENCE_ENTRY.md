# BATCH-201 — Evidence Entry

- **Batch ID:** BATCH-201
- **Short Topic:** PoeCore Phase 2 Setup
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Review Status:** REVIEWED
- **Source Type:** derived repo-migration summary
- **Primary Domain:** repo_structure_and_builder_runtime
- **Roadmap Tags:**
  - PHASE_1_CORE_ALIGNMENT
  - PHASE_2_COMPILER_IMPACT
  - PHASE_3_DOCUMENTATION_IMPACT
  - PHASE_4_SKILL_ALIGNMENT
  - PHASE_5_PRD_AND_STAGING

## Summary
Repo-migration batch moving toward canonical per-block files under `data/blocks/{MOLT_TYPE}/`, regenerating manifests from that source, unpacking autoblocks, clarifying stack/sleeve/schema distinctions, and surfacing unresolved semantics around `Deployment`, `Merge`, and Poe integration into the builder.

## Usefulness
- very strong for repo cleanup and builder runtime structure
- strong for compiler/input normalization
- strong for docs reconciliation
- strong for Poe helper integration planning
- medium ambiguity around final type semantics

## Key Caution
The repo structure direction is strong, but key semantics around `Deployment`, `Merge`, and the final Poe builder bridge remain unresolved.
