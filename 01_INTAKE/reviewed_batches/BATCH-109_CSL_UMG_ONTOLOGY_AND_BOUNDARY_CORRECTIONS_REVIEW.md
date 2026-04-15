# BATCH-109 — CSL, UMG, Ontology, and Boundary Corrections Review

## Batch Overview
- **Batch ID:** BATCH-109
- **Source type:** Derived extraction / handoff note
- **Review status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary domain:** core ontology, terminology correction, and compiler/runtime boundary clarification
- **Canon status:** Not canonized
- **Reason for intake:** The source concentrates high-value semantic correction around CSL, UMG, CIR, RuntimeSpec, Trace, PCL, S1+, and S2′, with direct impact on glossary stability and anti-drift documentation.

## Source Snapshot
- The source describes a correction-oriented conversation focused on stabilizing UMG architecture language.
- The central correction is that CSL should not be described as a compilable language.
- The source moves toward a stricter glossary that separates jurisdictional layers, framework behavior, runtime artifacts, and executor behavior.
- The source is not a raw transcript. It is an extracted summary and must therefore be treated as evidence with preserved uncertainty.

## Chat-Level Summary
This batch is primarily an ontology repair packet. It tightens the containment hierarchy among Governance, CSL, UMG, CIR, Compiler, RuntimeSpec, Trace, PCL, S1+, S2′, and Executor. Its most important correction is that CSL is a non-executing jurisdictional layer rather than a conventional language or a thing that compiles into CIR. UMG remains the framework/paradigm that resolves and binds cognition inside that admissible space.

## UMG-Relevant Extraction

### Core semantic signal
- UMG is framed as a paradigm/framework for structuring cognition, not as a model, runtime, or agent.
- Cognition is treated as explicit, swappable, auditable, and executor-independent.
- CSL is corrected into a jurisdictional layer that defines admissible cognitive space.
- S2′ is described as a regime enabled by UMG within CSL.
- Governance remains above CSL and UMG.

### MOLT / cognition-unit signal
- MOLT is treated as a classification grammar for semantic role, authority, and precedence.
- Example types listed in the source:
  - Trigger
  - Directive
  - Instruction
  - Subject
  - Primary
  - Philosophy
  - Blueprint
- Blocks gain meaning through composition and resolution, not in isolation.
- Stacks encode vertical authority ordering.

### Composition signal
- Block = smallest explicit unit of cognition.
- Stack = vertical composition of blocks across MOLT roles.
- Synthesis = resolution of multiple blocks/stacks into a higher-order artifact.
- NeoBlock = synthesized, reusable, compressed cognition with preserved traceability.

### Compiler / runtime boundary signal
- Rejected language:
  - CSL compiles into CIR
  - CSL emits CIR
  - CSL transforms into runtime artifacts
- Stabilized language:
  - CIR is instantiated and validated within CSL
  - UMG Compiler is the pre-runtime resolution and binding engine
  - RuntimeSpec is the executor-facing envelope
  - Trace is the audit artifact
  - PCL loads/enforces RuntimeSpec during execution

### Governance / safety signal
- Governance is supreme authority and may enable, disable, or invalidate cognition before resolution/execution.
- RuntimeSpec bounds allowed and forbidden reasoning moves.
- Executors do not own cognition; they operate within the resolved envelope.

## Independent Review
This batch is high-value evidence for the control project because it repairs a category error that would otherwise contaminate glossary language, compiler descriptions, and external-facing documentation. It is especially important for Phase 1 and Phase 3 because the correction reaches both semantics and spec language.

The batch should not be over-promoted. It is still a derivative summary, and some terms remain sensitive even after correction. In particular, the retained use of “UMG Compiler” alongside an anti-compilation stance for CSL needs careful wording discipline. This is strong evidence for canon-cleanup work, not a final canon file by itself.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - CSL as layer, not language
  - UMG within CSL
  - Governance above CSL/UMG
  - clarified relation among CIR, RuntimeSpec, Trace, PCL, S1+, S2′
- **PHASE_2_COMPILER_IMPACT**
  - compiler wording constrained to UMG-level resolution/binding
  - remove CSL-as-input compilation language
  - preserve distinction between admissibility and resolution
- **PHASE_3_DOCUMENTATION_IMPACT**
  - glossary repair
  - architecture summary repair
  - anti-leakage wording for external docs/specs
- **PHASE_4_SKILL_ALIGNMENT**
  - executor/agent framing should not claim cognition ownership
  - runtime skills should reference RuntimeSpec/Trace correctly
- **PHASE_5_PRD_AND_STAGING**
  - safer public-facing explanation of architecture
  - terminology migration requirements before broader release packaging

## Action Outcome
- Accepted as evidence.
- Optional extracts added for:
  - compiler/runtime boundary impact
  - blocks/MOLT/ontology impact
  - contradiction flags
- No canon promotion performed.
- No implementation semantics beyond what the source supports were added.

## Recommended Next Decision
Freeze a control-room terminology correction pack that:
1. permanently replaces “Cognitive Specification Language” with “Cognitive Specification Layer” where jurisdiction is intended,
2. removes all “CSL → CIR compilation” language,
3. clarifies that compiler behavior belongs to UMG-level resolution/binding, not CSL behavior.
