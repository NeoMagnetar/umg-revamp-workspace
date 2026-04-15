# BATCH-043 — Instruction Layer and Presentation Error Taxonomy Review

## Batch Overview
- **Batch ID:** BATCH-043
- **Topic:** Instruction-layer control, governance continuity, and presentation-error classification
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Source Condition:** Derivative summary, not raw transcript
- **Canon Status:** Evidence only; not promoted to canon

## Source Snapshot
- The source begins with a system-integrity check of the main Poe sleeve and its governance state.
- It then shifts into crafting a public-facing explanation of the role of the custom/project instruction layer in UMG.
- A formatting failure occurs when a reply is emitted outside the required envelope.
- The source diagnoses that event as a presentation-layer issue rather than a governance mutation, then regenerates the explanation inside proper sleeve structure.

## Chat-Level Summary
This batch is primarily about control-surface explanation and structural fault diagnosis. It argues that prompts and stacks are not the full story: the instruction layer governs persistence, composition, and long-horizon constraint behavior across frameworks. Its strongest operational contribution is the distinction between a genuine governance failure and a presentation-only compliance failure. The named category `PRESENTATION_ERROR_ONLY` becomes the key artifact: governance can remain stable while output formatting breaks, and recovery should preserve continuity rather than imply state mutation.

## UMG-Relevant Extraction
### Instruction layer framing
- The instruction layer is treated as the persistent control substrate rather than decorative text.
- Prompts are framed as output generators.
- Stacks are framed as reasoning organizers.
- The instruction layer governs how frameworks interact, persist, and constrain each other over time.

### Governance continuity
- Governance is explicitly checked and reported as intact.
- The active sleeve remains stable.
- Authority does not shift.
- Safety does not degrade.

### Presentation failure taxonomy
- The omitted envelope is treated as a rendering/compliance error.
- The batch introduces `PRESENTATION_ERROR_ONLY` as a distinct failure class.
- Recovery is continuity-preserving: restore the envelope on the next turn without implying governance mutation.

### Runtime implications
- The source implies a formal runtime classification path:
  1. classify the error
  2. preserve sleeve/governance continuity
  3. restore structural compliance
- A lightweight pre-emission self-check is suggested as a future mitigation.

## Independent Review
This is a strong evidence batch for separating control-plane failures from output-plane failures. Its biggest value is not new MOLT semantics, but error-taxonomy clarity. The distinction matters operationally: if every formatting miss is treated like a governance breach, the system becomes noisy, misleading, and unstable at the diagnostic layer. `PRESENTATION_ERROR_ONLY` is therefore a useful candidate for a continuity-preserving runtime error class.

The source also adds a valuable public-explanation frame: UMG’s leverage does not come from prompt stacking alone, but from the instruction/policy layer that controls persistence, interaction, and constraint behavior across frameworks. That idea is still partially rhetorical here rather than fully formalized in compiler terms, so it should remain evidence until codified more directly.

## Roadmap Mapping
### PHASE_1_CORE_ALIGNMENT
- Reinforces that governance continuity and presentation rendering are distinct layers.
- Supports cleaner boundaries between sleeve state, authority state, and output shape.

### PHASE_2_COMPILER_IMPACT
- Suggests a formal error class for envelope/render noncompliance.
- Suggests a lightweight pre-emission envelope/self-check trigger.

### PHASE_3_DOCUMENTATION_IMPACT
- Strong candidate language for explaining instruction-layer control.
- Supports documentation for failure taxonomy and recovery semantics.

### PHASE_4_SKILL_ALIGNMENT
- Relevant to skills that must preserve envelope structure under stable governance.
- Useful for any skill that generates public explanations while staying inside sleeve discipline.

### PHASE_5_PRD_AND_STAGING
- Supports a staged runtime/error-taxonomy story.
- Useful for explaining why structural compliance recovery does not imply state reset or governance breach.

## Action Outcome
- Accepted as evidence.
- Kept non-canonical.
- Optional extracts justified for compiler/runtime and sleeve/governance surfaces.

## Recommended Next Decision
Define a formal runtime error taxonomy that explicitly separates:
- governance failure
- sleeve/state mutation
- presentation/rendering failure
- external tool/access failure

`PRESENTATION_ERROR_ONLY` is the obvious first candidate for formalization.
