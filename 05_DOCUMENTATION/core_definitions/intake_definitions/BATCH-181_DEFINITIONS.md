# BATCH-181 - Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived block-generator and repo-automation summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Terms
Canonical Block Template
The authoritative schema definition a generated UMG block must conform to in order to be builder-readable, runtime-usable, and semantically meaningful.

Cantocore Identity String
Compressed internal semantic identifier tying block identity to role and function, such as SUBJ:... or INST:....

Role-Aware Generation
Generation process that infers or assigns molt_type based on block purpose and then uses that role for folder placement and downstream semantics.

Workflow-Native Generation
External generation path using scripts, Poe/API/Bolt, or GitHub workflows rather than relying on one-shot in-chat materialization.

## Runtime and Safety Terms
Repo-Safe Mutation
Operational rule that automation must not casually modify critical runtime files or executors without validation, rollback thinking, and trust preservation.

Generator Path Ambiguity
Open architectural uncertainty about whether the canonical block generator should live primarily in scripts, GitHub Actions, Poe terminal runtime, Bolt/API services, or a master-source workflow.
