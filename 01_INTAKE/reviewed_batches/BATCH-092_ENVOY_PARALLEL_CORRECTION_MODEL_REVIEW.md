# BATCH-092 Envoy Parallel Correction Model Review

## Batch Overview
- Batch ID: BATCH-092
- Source title: 092 Envoy Parallel Correction Model
- Source type: derived extraction / handoff note, not raw transcript
- Review status: REVIEWED
- Disposition: ACCEPT_AS_EVIDENCE
- Primary domain: core semantics + multi-agent stack coordination
- Confidence posture: medium for extraction fidelity, lower for canon strength because the source is already summarized and partly assistant-shaped

## Source Snapshot
- Input appears to be a structured extraction summary of a prior conversation about "snap stack merge potential" and parallel envoys.
- The source explicitly frames itself as "UMG Extraction Request Template Output for This Conversation."
- The source includes chat overview, relevance summary, categorized extraction, high-value candidates, ambiguity flags, and a handoff summary.
- Because this is not a raw transcript, exact wording provenance is mixed: some statements appear user-originated, some assistant-originated, and some are synthesized by the source author.

## Chat-Level Summary
The batch centers on a tandem multi-agent model inside UMG. It introduces "envoys" as the plural label for multiple agents sharing one mission or stack context, proposes a driver/navigator operating pattern, and describes an "anti-snap" correction behavior where either envoy can redirect the other back toward mission adherence. It also links this discussion to block/sleeve/stack semantics, MOLT context structure, and output-envelope constraints. The batch does not settle final policy; it mostly concentrates design pressure on merge semantics, shared stack-space meaning, correction authority, and documentation/runtime implications.

## UMG-Relevant Extraction
### Source-backed semantic candidates
- "Agent" / "bot" remain acceptable singular language.
- "Envoys" is proposed as the plural designation for multiple agents working together in one mission/stack context.
- A block can map 1:1 to an agent.
- A sleeve can map 1:1 to an agent.
- A stack is asserted as inherently multi-agent rather than singleton.
- Envoys can share one stack-space while holding different task assignments inside the same plan.

### Source-backed structure and schema pressure
- MOLT Map is treated as a defined context snapshot artifact.
- Named MOLT fields in the batch: Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint(optional).
- Omitted fields are expected to be explicitly marked "n/a."
- Trigger is implicitly pressured to support deviation / correction events.

### Source-backed runtime and workflow candidates
- Driver/navigator envoy pairing is presented as a reusable tandem pattern.
- Mutual correction / "anti-snap" is presented as a runtime behavior candidate.
- Shared mission state, periodic synchronization, and arbitration are named as implementation hooks, but these are exploratory rather than final.

### Source-backed ambiguity and risk
- "Snap stack merge" is not fully defined.
- "Shared space or stack" is not operationally defined.
- Block, sleeve, and agent relations remain under-specified.
- Mutual correction may create oscillation unless thresholds / authority rules are formalized.
- Some direction appears assistant-proposed and should not be upgraded to canon from this batch alone.

## Independent Review
This is a useful evidence batch because it concentrates several emerging UMG pressures into one place: plural-agent naming, stack plurality, correction semantics, MOLT snapshot formalization, and workflow implications for tandem agents. The strongest value is not final wording but problem localization. The batch is definition-rich, but it remains a secondary artifact. It should be treated as a synthesis lead for Phase 1 through Phase 4 review, not as an approved semantic decision set.

The most stable evidence from this batch is:
1. There is active pressure to define "envoys" distinctly from generic agents.
2. There is active pressure to clarify whether stacks are always plural.
3. There is active pressure to define how correction, merge, and divergence triggers interact.
4. There is active pressure to document MOLT as a stricter schema rather than a loose context note.

## Roadmap Mapping
- PHASE_1_CORE_ALIGNMENT
  - envoy terminology
  - stack plurality claim
  - merge / trigger semantics
  - block / sleeve / agent relation clarity
- PHASE_2_COMPILER_IMPACT
  - divergence detection
  - correction triggers
  - arbitration logic
  - traceability for snap events
- PHASE_3_DOCUMENTATION_IMPACT
  - glossary updates
  - MOLT schema formalization
  - output-envelope explanation
- PHASE_4_SKILL_ALIGNMENT
  - driver / navigator tandem workflow
  - bidirectional correction etiquette
- PHASE_5_PRD_AND_STAGING
  - future debug / observability concepts for correction events

## Action Outcome
- Accepted as evidence.
- Frozen into Stage 1 artifact pack.
- Optional extracts added because the batch contains clearly separable compiler/runtime pressure and block/MOLT-specific definitional content.
- Not promoted to canon.
- Not marked EXPORT_CANDIDATE.

## Recommended Next Decision
Define whether "envoys" is only a plural naming convention or a real runtime grouping concept with formal constraints on stacks, shared state, and correction authority.
