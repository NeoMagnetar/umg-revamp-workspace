# BATCH-136 — SemVer Instruction Block Review

## Batch Overview
Batch ID: BATCH-136  
Source Type: raw structured block artifact (JSON), not a transcript summary  
Working Topic: SemVer instruction block, block schema shape, CantoCore instruction encoding, schema-to-canon alignment  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a single JSON block artifact with:
- `block_id`: `semver_instruction_v1`
- label: `Semantic Versioning 2.0.0 Rules`
- category: `Software.Versioning`
- `molt_type`: `Instruction`
- CantoCore rule lines covering SemVer format, bump rules, prerelease/build metadata, precedence, phase rules, helpers, regex validation, and dependency-range example.

The block also includes non-core fields such as:
- `snap_config`
- `merge_logic`
- `ledger`
- `display`
- `editable_fields`
- `example_block_data`
- several empty extension arrays

Because this is a raw artifact rather than a retrospective summary, it is strong evidence of current block-shape and block-authoring practice. It should still remain evidence rather than canon until aligned against current UMG definitions and compiler expectations.

## Chat-Level Summary
This batch provides a compact but high-signal example of a domain-specific Instruction block expressed as a structured UMG-style artifact.
Its strongest value is not SemVer itself, but the block form:
a named block with explicit MOLT type, description, tags, ledger, editable fields, display metadata, and a dense instruction payload under `cantocore`.
The artifact also exposes likely canon-alignment tensions:
field naming conventions,
whether category metadata belongs at the semantic layer,
how UI/display/snap metadata should be separated from compiler semantics,
and whether a field such as `merge_logic` belongs on an Instruction block in this form.
The content itself is crisp and bounded: it behaves like a real Instruction block rather than drifting into philosophy, blueprint, or governance language.

## UMG-Relevant Extraction
The block is explicitly marked as `molt_type: Instruction`.
The payload is an operational rule set for software versioning, which fits Instruction much better than Philosophy, Blueprint, or Subject.
The CantoCore section is terse, machine-friendly, and procedural.
The block includes concrete instruction content for:
SemVer format,
public API declaration,
release immutability,
MAJOR/MINOR/PATCH bump conditions,
prerelease and build metadata handling,
precedence rules,
0.y.z versus 1.0.0 phase meaning,
helper aliasing,
regex validation,
and dependency range example.

The artifact shape also includes schema-like metadata:
block id,
label,
category,
description,
tags,
ledger,
display config,
editable fields,
example data,
and extension arrays.

The source therefore acts as:
1. an Instruction block example
2. a block-schema example
3. a possible compiler/frontend contract candidate
4. a canon-alignment stress test

The block stays role-pure overall:
it specifies rules and procedures rather than values, worldview, or output formatting.
The example data provides a concrete application example without changing the block’s primary function.

## Independent Review
This is a strong small-batch artifact because it is concrete, bounded, and already close to implementation form.
The SemVer content is well suited to an Instruction block: it encodes operational versioning logic rather than persona or stylistic drift.
The most important Stage 1 value, however, is schema pressure.
This artifact shows the project a plausible real-world block payload plus a practical outer wrapper, and therefore reveals where the project still needs sharper decisions about:
semantic fields versus renderer/UI fields,
compiler-relevant metadata versus authoring convenience metadata,
and how portable a block should be across builder, compiler, and storage layers.

The block appears especially useful as evidence for block-native software/process instruction artifacts.
Main cautions:
- `merge_logic: instruction_overrides_subject` may encode semantic/authority assumptions that need canon review.
- `snap_config`, `display`, and editable-field settings may belong to a frontend/persistence layer rather than canonical block semantics.
- `ledger.created_at: AUTO` suggests runtime population behavior that should be standardized if kept.
- empty extension arrays may be useful operationally but are not necessarily canon-worthy fields.

## Roadmap Mapping
Primary domain: block schema discipline and instruction-block authoring

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING

Key phase implications:
Phase 1: useful evidence for what a role-pure Instruction block looks like in practice.
Phase 2: exposes candidate block-schema fields that need compiler/storage/frontend boundary decisions.
Phase 3: provides documentation-ready example material for Instruction blocks and field separation rules.
Phase 4: useful for skill/block packaging patterns where domain rules are encoded as bounded instruction artifacts.
Phase 5: informs PRD/spec work for persisted block JSON, editability, and authoring/runtime metadata.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains a real block schema shape, role-specific content, and multiple canon-boundary questions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. canonical block JSON field set
2. semantic fields versus UI/display/persistence fields
3. treatment of `cantocore` as payload surface
4. role-pure Instruction block guidance
5. whether `merge_logic` belongs at block level
