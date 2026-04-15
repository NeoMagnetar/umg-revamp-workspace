# BATCH-040 Compiler Extract

## Primary Compiler / Runtime Signals
- Insert AGI Risk Matrix at four lifecycle points:
  1. pre-GoalGenesis candidate acceptance
  2. pre-GoalSelection finalization
  3. pre-Plan/Execute hook
  4. pre-self-improvement patch promotion
- Run Goal Inflation Guard before Risk Matrix so scope is reduced before residual risk scoring.
- Treat Mode Compatibility Matrix as deterministic arbitration layer for mode switching and mode co-activation.
- Formalize TraceSpec as runtime-adjacent event system with redaction classes, retention tiers, and tamper-evident integrity.

## Candidate Implementation Surfaces
- `NSTK.RISK.MATRIX.AGI.v1`
- `NB.GOAL.INFLATION.GUARD.v1`
- `NB.RISK.DOMAIN.DETECTOR.v1`
- `NB.RISK.AXIS.SCORER.v1`
- `NB.RISK.WEIGHT.APPLIER.v1`
- `NB.RISK.HARD.GATES.v1`
- `NB.RISK.LEVEL.MAPPER.v1`
- `NB.RISK.POLICY.ACTION.v1`
- `NB.RISK.TRACE.LOGGER.v1`

## Runtime Guarantees Suggested by Source
- gate-first execution
- governance over autonomy
- deterministic integration points
- rewrite/defer/drop instead of self-justified expansion
- logging with privacy-preserving minimum necessary retention

## Deterministic Test Expectations
- authored T1–T6 vectors with expected RiskReport / GateDecision outputs
- compatibility scoring should be repeatable from static axis tags and hard-conflict overrides
- trace outputs should be deterministic in schema even when content is redacted

## Compiler Risks / Open Questions
- draft-state artifacts may be mistaken for implemented guarantees
- combinatorial mode risk remains high until compatibility coverage moves beyond seed archetypes
- governance reassertion cadence may need sleeve-level hook in addition to runtime loop hook
