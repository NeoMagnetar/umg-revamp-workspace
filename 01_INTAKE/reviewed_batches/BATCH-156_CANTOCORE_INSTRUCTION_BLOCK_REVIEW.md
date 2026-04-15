# BATCH-156 Review — CantoCore Instruction Block

## Batch Overview
This batch is a strong Stage 1 evidence source for public-facing UMG/NEOCORE documentation language, draft block schema design, and an early compiler/runtime narrative linking JSON blocks to Mojo/Max Compute build outputs. The source is not a stabilized specification. It is a mixed artifact containing example schema, README-style framing, aspirational repo language, and interpretive merge/priority explanations. It should therefore be preserved as evidence and organizational input, not promoted to canon.

## Source Snapshot
- Source type: pasted batch summary / handoff memo
- Core subject: presentable UMG/NEOCORE block format and GitHub-facing repo documentation
- Main artifacts described:
  - example `Instruction` block JSON
  - README-style documentation for `UMG_NEOCORE`
  - candidate public repo positioning
  - candidate compile/runtime pipeline
- Primary emphasis:
  - block schema
  - snap / stack / merge behavior
  - block builder UI framing
  - Mojo / Max Compute execution path
  - creator-ecosystem and possible web3 distribution framing

## Faithful Chat-Level Summary
The chat started by defining a polished UMG/NEOCORE block format around an example `Instruction` block. That example included metadata, snap rules, merge logic, display fields, ledger metadata, runtime flags, and Mojo code-module references. The discussion then expanded into README-style repository documentation for a public `UMG_NEOCORE` repo. In that framing, blocks auto-recognize each other, snap into stacks, merge according to priority and conflict rules, remain editable in a block-builder UI, and may eventually compile into executable kernels. The repo positioning also presented UMG as a modular creation ecosystem in which blocks can be imported, remixed, distributed, and potentially connected to a web3-native ownership/distribution layer.

## UMG-Relevant Extraction
### 1. Semantics and terminology
The source contains candidate definitions for Block, Stack, Sleeve, Snap, Merge Engine, Cantocore, Mojo, and Max Compute. It also proposes a priority ladder and runtime trigger examples. These are highly relevant to Phase 1 semantic stabilization and Phase 3 documentation impact, but they remain draft language.

### 2. Block schema design
The source provides a concrete candidate block structure with fields such as:
- `block_id`
- `label`
- `category`
- `description`
- `molt_type`
- `tags`
- `cantocore`
- `snap_config`
- `merge_logic`
- `ledger`
- `display`
- `editable_fields`
- `example_block_data`
- `code_modules`
- `runtime_behavior_flags`
- `integration_layer`
- `agent_orchestration`
- `future_extensions`

This is one of the stronger schema-oriented sources in the current range because it moves beyond abstract doctrine into draft object shape.

### 3. Blocks/MOLT structure
The source explicitly uses `molt_type` and lists role names including Instruction, Primary, Subject, Blueprint, Philosophy, Directive, Overlay, Trigger Block, and Guardrail. That makes it directly relevant to any future effort to stabilize block taxonomies, role semantics, and composition behavior.

### 4. Composition logic
The source presents a snap -> stack -> merge progression, with vertical vs horizontal snap targets, merge priority, dependency handling, and conflict strategies such as override, concat_array, diagnose, and abort. This is useful evidence for composition-language design, but the merge ladder appears to be assistant-drafted and is not yet user-ratified.

### 5. Compiler/runtime narrative
The source ties block JSON to code modules, Mojo, Max Compute, WASM/binary compilation, sealing artifacts back into blocks, and runtime loading via WASI/edge runtime. This is a high-value bridge between semantics and implementation, but it is described as intended architecture rather than demonstrated execution.

### 6. Public-facing repo/documentation framing
The source contributes a README structure and public language for a block-native software creation engine and creator ecosystem. This is relevant to PRD and documentation staging, but some claims are aspirational and may overstate current implementation maturity.

## Independent Review
### Evidence quality
- Structural value: high
- Canon reliability: medium-low
- Implementation proof: low
- Documentation value: high
- Compiler/value as direction-setting evidence: high

### Why it matters
This batch is important because it gathers in one place several surfaces that must eventually align:
1. semantic vocabulary
2. block schema shape
3. composition behavior
4. compiler/runtime aspirations
5. public repo framing

That combination makes it useful for the revamp even though none of the individual elements should be treated as final on their own.

### What should be trusted most
The strongest signals are:
- the existence of a schema-oriented block composition draft
- the importance of `molt_type`, snap rules, merge logic, and display/runtime separation
- the need to separate documentation aspiration from current implementation capability
- the need to define an implementation matrix before public-facing claims harden

### What should be treated cautiously
- any specific merge ladder
- claims that blocks can replace HTML/CSS/JS
- claims that Mojo/Max Compute pipeline is already proven
- `.sleeve` bundle assumptions
- web3 ecosystem framing as if it were implementation-ready
- partially defined control constructs like VSS and Guardrail without formal definitions

## Roadmap Mapping
### Phase 1 — Core Alignment
Strongly relevant to:
- Trigger semantics
- Priority semantics
- Merge semantics
- Bundle semantics
- NeoBlock composition rules
- reserved / meta MOLT handling

### Phase 2 — Compiler Impact
Relevant to:
- module attachment model
- compile target and artifact sealing concept
- runtime loading surfaces
- future compiler task specification

### Phase 3 — Documentation Impact
Strongly relevant to:
- block / NeoBlock / NeoStack explanations
- glossary and definition cleanup
- diagramming and public README language
- separating current capability from future direction

### Phase 4 — Skill Alignment
Moderately relevant due to:
- `agent_orchestration`
- `integration_layer`
- sleeve-as-agent framing

### Phase 5 — PRD and Staging
Relevant to:
- block-native creator ecosystem positioning
- implementation-maturity matrix
- ecosystem ambitions vs release-scope boundaries

## Recommended Next Decision
Do not promote this schema or README language directly. Hold it as a strong evidence batch and use it to drive:
1. a definitions audit,
2. a block schema comparison pass,
3. a compiler feasibility separation between current, near-term, and aspirational claims.

## Disposition
**ACCEPT_AS_EVIDENCE**

Reason:
The batch is coherent, high-value, and rich in reusable language and structure, but it is not sufficiently stabilized for canonical promotion. It is best preserved as evidence for semantic alignment, schema design, documentation revision, and compiler planning.
