# BATCH-125 — Replit App Setup / Studio Recovery Review

## Batch Overview
Batch ID: BATCH-125  
Source Type: derived summary / extraction note, not a raw transcript  
Working Topic: Replit app setup, UMG Studio Block Tutorial recovery, UI failure mode, release discipline  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured summary of a conversation around stabilizing and publishing a UMG Studio Block Tutorial v0, with emphasis on ReactFlow graph rendering, mobile layout failures, recovery attempts, and later UMG-aligned reflection.
It reports repeated layout and rendering mutations, an eventual broken application state, and a final pivot toward extraction and process review rather than continued speculative fixing.
Because this is a derived handoff-style summary rather than a raw code diff or raw transcript, it preserves useful project signal but should be treated as summarized evidence rather than direct implementation truth.

## Chat-Level Summary
This batch documents a practical breakdown in a UMG-adjacent implementation surface.
The key lesson is procedural rather than purely conceptual: repeated, multi-layer mutation without strong trace or baseline discipline destabilized the system.
The source also captures partial implementations of UMG concepts inside the tutorial flow, including MOLT spine construction, NeoBlock compression, NeoStack composition, sleeve creation, RuntimeSpec + Trace output, and Inspector-based gating.
The conversation ultimately becomes a failure-mode case study for deterministic iteration, bounded agent behavior, release freezing, and the separation between specification, runtime behavior, and UI architecture.

## UMG-Relevant Extraction
The batch frames “baseline” as a stable container or known-good state, which maps closely to sleeve-level preservation and controlled mutation.
It reaffirms the canonical seven-role MOLT stack: Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.
It introduces a “spine” concept: one block per MOLT role as a completeness baseline, with extras allowed but not required for completion.
Trigger logic appears as tutorial-step progression and state transitions rather than explicit authored Trigger blocks.
PriorityOrder appears as an integer field and UI control, but is not yet fully integrated into runtime semantics.
Merge and bundle are present but only partially distinguished; current implementation behavior is simplified and snapshot-oriented.
NeoBlock is treated as a compressed structure derived from a full MOLT spine and storing source linkage plus a MOLT snapshot.
NeoStack is treated as a composition artifact created from NeoBlocks and then named before sleeve creation.
Sleeve is the highest artifact in the tutorial flow, though runtime resleeving remains future-facing.
Governance appears indirectly through gating, validation, disabled actions, and a dominant-snapshot rule rather than a formal governance subsystem.
RuntimeSpec + Trace generation exists in a compiler-like form, though an explicit compiler abstraction layer is not yet formalized.
The batch strongly argues for trace gates, minimal mutation cycles, bounded agent behavior, and feature freeze before release.

## Independent Review
This batch is valuable less as canonical semantics and more as implementation/process evidence.
Its strongest contribution is a grounded case study showing what goes wrong when change sequencing becomes non-deterministic and inadequately traced.
That makes it especially useful for Phase 2, Phase 4, and Phase 5 work, where compiler discipline, agent constraints, release gates, and trace completeness need operational grounding.
Several semantic statements are also worth preserving, particularly the seven-role MOLT ordering, the NeoBlock/NeoStack/Sleeve progression, and the separation between internal state and rendered output.
However, caution is required because some terms in this batch are implementation-local or provisional, including “spine,” “baseline sleeve,” and “trace gate,” and some described behaviors are explicitly partial or incomplete rather than stable UMG canon.

## Roadmap Mapping
Primary domain: implementation failure analysis with compiler/runtime/process implications

Roadmap phases touched:
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION

Key phase implications:
Phase 2: useful for trace completeness, composition formalization, and merge-vs-bundle clarification.
Phase 3: suggests documentation around baseline locking, trace-gated mutation, and failure-mode case studies.
Phase 4: directly supports bounded-agent workflow and stricter instruction templates.
Phase 5: reinforces feature freeze, static deployment preference, and scope control before release.
Phase 6: informs implementation staging discipline and recovery procedures for repo-level execution work.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, contradiction flags, and canon candidates are justified because the batch mixes partial implementation semantics with process lessons and explicit unresolved ambiguities.

## Recommended Next Decision
Control-room review should decide whether “baseline,” “trace gate,” and “spine blocks” remain implementation-local terminology or should be normalized into broader UMG documentation and compiler/process vocabulary.
