# BATCH-181 - UMG Block Generator Setup and Repo Automation Review

## Batch Overview
Batch ID: BATCH-181
Source Type: derived summary / block generation and runtime recovery consolidation
Working Topic: canonical block template authority, MOLT-aware generation, Poe terminal breakage, GitHub workflow uncertainty, spec-driven block generation
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source captures an attempt to operationalize UMG block generation inside a Git and GitHub workflow and then recover from repeated failures in repo state, workflow behavior, and Poe terminal execution.

The strongest recurring themes are:
- use the canonical UMG block template as the real authority
- generate real runtime-usable blocks from raw lists, YAML, docs, and category tables
- preserve meaningful MOLT typing rather than defaulting everything to Subject
- encode cantocore, snap_config, merge_logic, and ledger as part of real block semantics
- move generation into external workflow or tooling rather than depending on chat-scale manual expansion
- recover from brittle repo mutation after poe_executor.py was broken by invalid edits

## Chat-Level Summary
This batch is strongest as a practical block-generator setup source.

Its central contribution is that a UMG block is treated as a real structured semantic object that must be:
- template-faithful
- role-aware
- directory-aware
- builder-readable
- runtime-usable

The second strongest contribution is the generation boundary.
The chat repeatedly shows that large-scale block creation belongs in workflows, scripts, Poe/API/Bolt execution, or GitHub automation rather than in one-shot chat output.

The third strongest contribution is the operational safety lesson.
Invalid executor edits can take Poe terminal offline, which makes bounded mutation and spec-first agent work a project-critical requirement.

## UMG-Relevant Extraction

### Core UMG Semantics
A UMG block is treated as a structured JSON object with canonical fields such as:
- block_id
- label
- category
- description
- molt_type
- tags
- cantocore
- snap_config
- merge_logic
- ledger
- display
- code_modules
- runtime_behavior_flags
- agent_orchestration
- integration_layer
- future_extensions
- example_block_data

Blocks are treated as atomic units that must be semantically meaningful, builder-readable, and runtime-usable rather than placeholder stubs.

cantocore is treated as a compressed semantic identity string tied to role and purpose, with examples like SUBJ:STARTUP_PLAN and INST:COOLDOWN_TIMERS_FOR_REWARD_LOOPS.

### MOLT Roles / Taxonomy
The source explicitly preserves these active role classes:
- Primary
- Subject
- Instruction
- Blueprint
- Philosophy
- Directive
- Deployment
- Trigger
- Off

molt_type is not cosmetic. It determines functional role, categorization, and folder placement.

The source gives practical heuristics rather than a final full canonical inference table:
- plan or strategy-like categories lean toward Primary
- documentation, training, or process categories lean toward Instruction
- legal, compliance, or ethics material leans toward Philosophy
- other material may default to Subject when no stronger inference exists

### Trigger
Trigger is preserved as a legitimate block type even though concrete trigger rules are not finalized here.
Trigger is treated as a future runtime or event-based behavior layer that needs proper semantics and foldering.

### Priority
Priority is preserved indirectly through:
- fit_score in snap_config
- stack compatibility and ordering assumptions
- future merge and stack conflict behavior

fit_score: 100 is used as a practical default indicating full intended stack fit.

### Merge
merge_logic is part of the expected block schema even when blank in examples.
The source treats merge as a real long-term UMG concept connected to stack coexistence and composition.

### Bundle
Bundling is implied through large category-driven block sets generated into organized folders and later reused in workflows.
The ambition is clearly library-scale generation, even though no final bundle schema is frozen here.

### NeoBlock Composition
Each JSON UMG block functions as a NeoBlock-like compositional unit.
A block must:
- identify itself
- declare its role
- expose tags and cantocore
- participate in snap, merge, and stack logic
- preserve provenance via ledger

### NeoStack Architecture
snap_config is treated as a key mechanism for stack participation.
The example preserved in the source uses:
- snap_to: ["stack"]
- fit_score: 100

Instruction blocks are assumed to stack under broader layers such as Subject or Primary.

### Governance and Control
This batch strongly demonstrates governance needs:
- block generation should be controlled and deterministic
- the template is authoritative
- repo mutation should not be improvised
- partial workflows and casual executor edits are anti-patterns
- workflow authority and source-of-truth paths need consolidation

### Output Blueprint and Rendering Separation
The source preserves a strong distinction between:
- the semantic block template
- the scripts and workflows that generate files
- the directories where files live
- the runtime or builder that consumes them

The user explicitly asked for the exact template rather than more code, reinforcing that semantic schema and implementation vehicle are separate layers.

### Compiler and Runtime Logic
A major theme is that block generation should be automatable from:
- YAML
- plain text
- raw block-name lists
- source documents
- Google Docs or master docs

The desired runtime or compiler pattern is:
source material to semantic inference to template fill to runtime-ready JSON output

Runtime assumptions preserved in the source:
- relative paths from repo root
- GitHub Actions as a possible build executor
- Poe terminal agent as local interactive runtime
- generation belongs in external tooling rather than in-chat when scale increases

### Documentation and Spec Language
README_UMG_BLOCK_TEMPLATE.md is treated as the canonical schema reference.
The source adds practical field meaning around:
- molt_type
- cantocore
- snap_config
- merge_logic
- ledger

### Skill and Agent Workflow
The source repeatedly treats Poe as an agent that should be able to:
- parse block lists
- generate block files
- populate metadata
- write files into correct folders
- operate through terminal or workflow
- commit tasks

The repo references:
- poe_terminal_agent.py
- poe_executor.py
- scripts for building or filling blocks
- multiple GitHub workflows

A concrete failure is preserved:
invalid elif insertion broke poe_executor.py, taking Poe terminal offline.

### Safety and Bounded Agency
The batch gives a strong bounded-agency lesson:
- repo mutation should not casually touch core runtime files
- automation should preserve trust under deadline pressure
- the agent should follow direct instructions precisely
- mutation should be controlled, validated, and minimally disruptive

## Independent Review
This batch has high Stage 1 value because it records the exact practical requirements for making UMG block generation real at scale.

Its strongest contribution is not a final build pipeline.
It is the implementation pressure test:
- template authority
- MOLT-aware inference
- role-aware folder placement
- spec-driven generation
- repo-safe mutation boundaries

The source is also important because it reveals a recurring architectural conclusion:
large-scale block generation should be workflow-native and scalable beyond chat token limits.

## Roadmap Mapping
Primary domain: practical block generation setup, repo automation, and workflow-safe runtime behavior

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
1. canonical block-template authority language
2. authoritative MOLT inference rules for generation
3. workflow-native generation path versus chat-native generation path
4. repo mutation safety and rollback boundaries for Poe/GitHub automation
5. exact directory conventions for generated blocks and schema sources
