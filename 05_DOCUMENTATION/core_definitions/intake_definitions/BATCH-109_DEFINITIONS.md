# BATCH-109 — Definitions Extract

## Terminology, Meanings, and Candidate Definitions

### CSL
- Corrected meaning: **Cognitive Specification Layer**
- Defined here as an abstract, non-executing, jurisdictional category that defines where cognition may exist.
- Not a conventional language.
- Not a compiler input.
- Does not emit, compile, transform, or execute artifacts.

### UMG
- Framework/paradigm operating within CSL.
- Specifies, resolves, and binds cognition into executor-facing form.
- Not a runtime, model, or agent.

### Cognition
- Treated as a first-class, external, auditable artifact rather than something smeared across prompts or embedded inside agent code.

### MOLT
- Classification grammar for semantic role, authority, and precedence.
- Defines semantic position and authority interaction, not behavior itself.

### Block
- Smallest explicit unit of cognition.
- Inert on its own, non-executing, MOLT-typed.

### Stack
- Vertical composition of blocks across MOLT types with internal authority ordering.

### Synthesis
- Process of resolving multiple blocks/stacks into a higher-order artifact while preserving authority, constraints, and traceability.

### NeoBlock
- Synthesized, compressed, reusable cognitive artifact created from resolved composition.

### CIR
- Concrete cognitive artifact instantiated and validated within the jurisdiction of CSL.
- Should not be described as “compiled from CSL.”

### UMG Compiler
- Pre-runtime resolution and binding engine operating on cognitive artifacts admissible under CSL.
- Terminology-sensitive term: keep compiler behavior attached to UMG, not CSL.

### RuntimeSpec
- Executor-facing cognitive envelope that constrains allowed moves, forbidden moves, structure, and priority ordering.

### Trace
- Audit artifact recording what was considered, what prevailed or was suppressed, and why conflicts resolved as they did.

### PCL
- Operational layer that loads RuntimeSpec and enforces cognitive constraints during execution.
- Does not author or resolve cognition.

### S1+
- Fast-path regime with dynamic context and lightweight cognitive constraints without full resolution.

### S2′
- Regime enabled by UMG within CSL where deliberate reasoning is driven by explicit, programmable cognition constrained by RuntimeSpec.

### Governance
- Supreme authority layer above UMG and CSL.
- May enable, disable, or invalidate cognition before resolution or execution.

### Executor
- System that performs reasoning or action within the constraints of RuntimeSpec.
- Examples may include LLMs, tool-using agents, or hybrid human-AI systems.

## Role Language / Architecture Language
- UMG: framework/paradigm
- CSL: jurisdictional layer
- CIR / RuntimeSpec / Trace: artifacts
- PCL / Executor: operational/runtime-facing layers
- Governance: supreme authority above architecture

## Definitional Candidates to Preserve Carefully
- “CSL never compiles, never transforms, never emits artifacts, and never executes.”
- “UMG operates within CSL to specify, resolve, and bind cognition.”
- “CIR is instantiated and validated within CSL.”
