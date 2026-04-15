# BATCH-104_WORLD_MODELS_VS_UMG_REVIEW

## Batch Overview
- **Batch ID:** BATCH-104
- **Short Topic:** World Models vs UMG
- **Source Type:** Derived extraction / handoff note, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** governance-first cognitive layering and world-model subsystem integration
- **Confidence Note:** This batch is comparatively coherent and structurally useful because it draws a strong distinction between prediction, planning, decision, and execution. Its main value is not proving that world-model integration already exists in UMG, but clarifying how such a subsystem could fit inside a governance-first cognitive architecture without collapsing UMG into simulation-only reasoning.

## Source Snapshot
- Source title: `104 World Models vs UMG`
- Source character: summarized extraction of a prior comparison chat
- Main themes surfaced by source:
  - comparison between external world-model research and UMG
  - explicit governance-first ordering from intent through execution
  - positioning world models as one subsystem inside a broader cognitive operating structure
  - candidate insertion points for simulation modules inside UMG
  - reinforcement of the distinction between prediction and decision
- Provenance caution:
  - source is a distilled comparison note rather than direct transcript evidence
  - the external world-model essay is represented through summary rather than inspected directly here
  - several integration ideas are candidate structures, not confirmed existing implementation

## Chat-Level Summary
This batch contributes a comparatively clean layering packet. It argues that **world models are predictive subsystems**, while **UMG is the broader cognitive operating system** that governs whether, when, and how predictive outputs affect planning or execution. The source gives a vertical ordering: **Intent → Governance → Context → World Model → Planning → Execution**, and repeatedly reinforces that governance must precede reasoning or simulation. The strongest contribution is therefore architectural separation: prediction does not equal decision, world-model outputs must pass through context/state handling and planning surfaces, and execution should remain downstream of governance and translation layers. This makes the batch useful for Phase 1 and Phase 2 work because it offers a clean way to integrate simulation capabilities without surrendering UMG's governance-first identity.

## UMG-Relevant Extraction
### Core semantics
- UMG is framed as a modular cognitive architecture rather than a single reasoning model.
- World models are positioned as a subsystem inside UMG, not as the whole architecture.
- Representation, governance, memory, planning, reasoning, and execution are separated.
- The source strongly reinforces that prediction and decision are not the same act.

### MOLT / block signal
- Context and State are associated with MOLT-like state mapping.
- MOLT is implicitly responsible for:
  - current situation
  - historical continuity
  - active constraints
  - agent state
- Candidate block families include:
  - WorldModelBlocks
  - PredictiveBlocks / StateMaps
  - Planning & Action Blocks
  - Governance Blocks
  - Memory / MOLT Blocks

### NeoStack / layering signal
- A full ordered vertical structure is proposed:
  - Human Intent
  - Interpretation / Framing
  - Governance & Alignment
  - Context & State (MOLT)
  - World Model / Simulation
  - Planning & Reasoning
  - Translation to Operations
  - Execution
- The packet treats this ordering as deterministic and legible rather than emergent.
- World-model logic is kept subordinate to governance and planning layers.

### Runtime / compiler signal
- Intent parsing starts the pipeline.
- Governance validates before simulation influences downstream behavior.
- Translation to operations acts as a boundary between reasoning/planning and executable action.
- A feedback loop from execution back into future state is implied.
- The packet implies a compilation path from intent through structured planning into executable output, even though no explicit compiler contract is finalized.

### Governance / control signal
- Governance precedes intelligence.
- Governance defines permissions, constraints, and authority checks.
- The world-model layer cannot directly self-authorize action.
- Safety is protected by separating predictive simulation from action execution.

### Documentation / product signal
- The batch contributes clean definitional language:
  - world models predict
  - UMG decides and governs
  - prediction does not equal decision
- It is useful for docs/spec work because the layer names are stable enough to compare against existing UMG stack language.
- It also creates a practical path for future subsystem rollout without reframing UMG as only a simulation architecture.

## Independent Review
This batch is best treated as a **layer-separation and subsystem-placement packet**. Its main usefulness is conceptual hygiene. It resists the common collapse where a predictive simulation model is treated as if it already includes governance, authority, and action policy. Instead, it gives UMG a broader role: UMG governs, holds state, frames context, plans, translates, and then executes.

That matters because recent batches already pressure UMG toward simulation, branching, and adaptive reasoning. This packet offers a disciplined way to absorb those pressures. A world model can exist, but it remains just one layer. It does not bypass governance, and it does not turn prediction into permission.

The main caution is implementation ambiguity. The packet does not define a formal interface for WorldModelBlocks, does not settle the boundary between PredictiveBlocks and WorldModelBlocks, and does not specify how state updates loop back into the model. So this source is high-value for architecture clarification, but not yet direct implementation canon.

## Roadmap Mapping
### PHASE_1_CORE_ALIGNMENT
- pressures clarification of:
  - governance-first ordering as core UMG identity
  - whether world models are first-class subsystems or optional advanced layers
  - how MOLT state maps differ from predictive simulation modules

### PHASE_2_COMPILER_IMPACT
- pressures need for:
  - formal runtime ordering from intent through execution
  - explicit translation layer between planning and operations
  - interfaces for simulation outputs entering planning/state surfaces
  - feedback loop definitions for execution results

### PHASE_3_DOCUMENTATION_IMPACT
- suggests documentation on:
  - difference between prediction and decision
  - UMG as cognitive operating system versus world-model subsystem
  - clean layer naming for governance, context, simulation, planning, and execution

### PHASE_4_SKILL_ALIGNMENT
- suggests:
  - pluggable WorldModelBlock skill behavior
  - planning skills that consume simulation outputs only after governance checks
  - tool/execution skills separated from simulation skills

### PHASE_5_PRD_AND_STAGING
- suggests:
  - staged rollout of world-model capability as subsystem addition
  - release planning that keeps governance visible even when simulation is introduced
  - modular insertion points for simulation-enhanced planning

## Action Outcome
- **Disposition chosen:** ACCEPT_AS_EVIDENCE
- **Why:** the batch contributes clear subsystem boundaries, clean governance-first ordering, and plausible insertion points for simulation capability, but it remains conceptual and does not finalize interfaces or implementation contracts.
- **Optional extracts justified:**
  - `COMPILER_EXTRACT` because the source strongly pressures a formal layered pipeline, translation boundary, and feedback path.
  - `BLOCKS_MOLT_EXTRACT` because the source names candidate world-model, state, planning, governance, and memory block families.
  - `NEOSTRUCTURE_EXTRACT` because the packet defines a full ordered vertical stack and clarifies subsystem placement within broader UMG architecture.

## Recommended Next Decision
Decide whether a World Model layer should be formalized as an optional pluggable subsystem between Context/State and Planning, or treated as a broader simulation capability folded into existing advanced runtime work.
