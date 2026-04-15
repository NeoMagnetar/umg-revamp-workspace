# BATCH-036 — Compiler / Runtime Extract

## Compiler-Facing Signal
This batch argues that major parts of UMG remain declarative until execution order, validation, state handling, and governance move into a true runtime/controller. Its strongest compiler/runtime contribution is not a narrow syntax rule, but a shift in where responsibility should live.

## Strongest Runtime Ideas
- externalize execution order from prompt text into controller logic
- externalize validation into ordered runtime stages
- externalize state persistence beyond single-turn generation
- keep governance enforceable outside mutable prompt behavior
- start with a minimal runtime rather than a maximal architecture

## Candidate Minimal Runtime Flow
1. user input
2. controller/orchestrator
3. stack selection / ordered execution
4. LLM calls
5. validation / next-stage routing
6. output emission

## Candidate First Runtime Scope
- context mapping
- reasoning
- output compiler

## Additional Runtime Candidate
- model identity / capability detection stack for adaptive sleeve and stack selection

## Compiler / Runtime Risks
- architecture bloat outrunning implementation
- prompt-only control logic overloading the model
- lack of explicit state management
- self-modification without enforced governance
- lack of real execution pipeline

## Recommended Later Audit Question
Which current responsibilities stay in prompt/spec form, and which must move into executable controller logic before the project can claim runtime progress?
