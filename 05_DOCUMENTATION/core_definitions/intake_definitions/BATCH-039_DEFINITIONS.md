# BATCH-039 — DEFINITIONS EXTRACT

## Terminology and Meanings

### Policy-Constrained Deterministic Agency Simulator
A framing for the current UMG architecture where agency is structured, scored, and bounded by explicit policy and runtime gates rather than allowed to expand autonomously.

### Governance Invariance
The expectation that governance constraints remain fixed and non-mutable during runtime operation and stress conditions.

### Drift Reanchor
A runtime recovery behavior in which measured persona/format/spec drift beyond threshold triggers re-anchoring to stable governing state.

### Anti-Thrash Lock
A runtime safeguard that prevents rapid oscillation or repeated unstable switching among candidate goals or modes.

### Stability Index (SI)
A composite evaluation metric proposed for the architecture using governance invariance, recursion boundedness, drift control strength, selection sensitivity, and adversarial resistance.

### Exclusive Identity Container
A sleeve property meaning sleeve identity remains singular/monolithic and is not blended in parallel with competing sleeves during conflict scenarios.

## Role Language
- **Trigger (TR):** activation condition or initiating event
- **Directive (DIR):** high-level mission / intended orientation
- **Instruction (INS):** specific procedural step or local action
- **Subject (SUB):** target domain/object/focus under reasoning
- **Primary (PRI):** dominant weighting or priority signal
- **Philosophy (PHI):** guiding stance or governing rationale
- **Blueprint (BP):** output structuring / render contract

## Architecture Language
### Sleeve
Identity layer / runtime envelope.

### NeoStack
Functional reasoning cluster / runtime stage group.

### Runtime Loop
Ordered execution cycle across goal genesis, goal selection, output, and optional bounded self-improvement.

### Queue-Based Concurrency
Constraint model with one active primary and bounded queued secondary goals rather than unconstrained parallel autonomy.

## Runtime / Compiler Language
### Hard Gate
A non-negotiable threshold or filter that must pass before scoring or action continues.

### Weighted Policy Model
Deterministic scoring framework combining utility, feasibility, risk, and alignment.

### Non-Authoritative Tool Output
A tool result that informs the system but may not bypass the controller; it must be re-evaluated through the gated pipeline.

### Formal Invariance Check
Proof-style reasoning used to test whether defined runtime invariants remain true under stress conditions.

## Definitional Candidates
- UMG = **policy-constrained deterministic agency simulator**
- **Determinism > Drift**
- **Bounded Agency > Autonomous Drift**
- **Controlled Tooling > Autonomous Expansion**
- sleeves are **exclusive identity containers**
- cross-sleeve conflict yields **deterministic arbitration**, not hybrid autonomy
