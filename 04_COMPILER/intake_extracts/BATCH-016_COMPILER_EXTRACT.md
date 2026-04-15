# BATCH-016_COMPILER_EXTRACT

## Compiler / Runtime-Relevant Signal
This batch does not define a full compiler path, but it isolates one concrete implementation pressure: governance and stack state need reliable declaration/reporting so they do not appear broken when still conceptually active.

## Candidate Compiler / Runtime Tasks
- strengthen active-state declaration
- strengthen governance/stack state rendering
- distinguish actual control state from reported state
- reduce state-visibility drift
- make governance visibility a first-class reporting concern rather than a cosmetic afterthought

## Confidence
Medium

## Notes
This is more reporting/runtime-surface guidance than deep compiler semantics.
