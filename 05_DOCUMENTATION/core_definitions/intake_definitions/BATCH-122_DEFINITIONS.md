# BATCH-122_DEFINITIONS

## Core Definitions Extract
- **UMG (Universal Modular Generation):** framework for constructing, planning, and generating cognitive processes as modular, inspectable artifacts prior to execution.
- **CSL (Cognitive Specification Layer):** non-executing pre-runtime jurisdiction where cognition is specified, resolved, versioned, and audited.
- **SO-CCP (Specification-Oriented Cognitive Control Plane):** upstream control plane for cognition specification, resolution, and compilation.
- **MOLT:** language for cognition used to express cognitive intent, constraints, priorities, and structure.
- **CIR (Cognitive Intermediate Representation):** compiled cognitive intermediate representation of resolved cognition.
- **RuntimeSpec:** enforceable runtime contract derived from CIR.
- **Decision Trace:** deterministic record of cognitive resolution and precedence handling; canonical replacement for older “trace audit” phrasing.
- **DCEP (Dynamic Context Engineering Protocol):** execution-time protocol assembling/applying MOLT-derived guidance for single-pass inference without planning or cognition construction.
- **S1:** reactive inference.
- **S1+:** guided reactive inference via DCEP.
- **S2′:** constructed deliberation governed by compiled artifacts.
- **AI Wrapper:** optional runtime mediation layer that does not define pre-execution cognition.
- **RCOL (Runtime Cognitive Orchestration Layer):** downstream runtime coordination layer for agents/tools/routing/memory, distinct from SO-CCP.

## Distinctions
- UMG != wrapper
- SO-CCP != RCOL
- MOLT != programming language
- MOLT != prompt language
- MOLT != policy-only language
- CIR != RuntimeSpec
- RuntimeSpec != Decision Trace
- DCEP != planning / compilation / cognition construction

## Candidate Canon Language
- “AGI is claimed as an architectural capability, not a behavioral guarantee.”
- “Runtime orchestration coordinates execution; SO-CCP governs cognition before execution as explicit artifacts.”
- “MOLT is a language for cognition: it specifies how reasoning is allowed to happen.”
