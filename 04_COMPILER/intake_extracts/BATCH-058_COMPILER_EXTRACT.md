# BATCH-058 Compiler Extract

## Scope
Runtime vocabulary and compiler-adjacent distinctions surfaced in a glossary-heavy batch

## Compiler-Relevant Findings
- CantoCore and Cyentcore were differentiated as separate layers rather than synonyms
- CEL runtime flow was described as:
  - UMG Blocks -> CEL Engine -> Mutational Blend -> VSS Filter -> Actionable Concepts
- VSS was framed as a formal scoring/filter stage with a default pass threshold concept
- Chaos Lens was described as conditionally active on loop-detection or flat-output conditions
- Priority was represented as active stack order plus overlay subordination to Alignment Core

## Candidate Tasks
1. Define a formal Cyentcore vs CantoCore boundary
2. Specify CEL pipeline inputs, outputs, and mutation constraints
3. Specify VSS score dimensions and pass/fail contract
4. Define overlay activation and precedence rules
5. Create trace/audit vocabulary for loadout visibility

## Risks
- some distinctions are conversationally strong but not yet normalized across docs
- origin-date claims should not enter compiler-facing docs without verification
- rhetorical framing may obscure exact runtime semantics

## Recommended Hold Line
Treat these items as spec candidates pending cross-document normalization.
