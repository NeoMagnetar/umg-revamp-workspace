# BATCH-020 — Compiler Extract

## Compiler Direction Signal
The batch makes compiler awareness foundational to the repo, but deliberately stages compiler work after bootstrap.

## Strongest Compiler Implications
### 1. Separate compiler phase
Do not collapse repo bootstrap and compiler upgrade into one step.
Handle them as distinct phases:
- repo bootstrap
- skill wrapper
- compiler integration
- canonical artifact generation

### 2. Explicit compiler paths
The batch expects compiler-aware structure such as:
- `compiler/`
- `scripts/compile-runtime.ts`
- `runtime/compile-output/`
- `runtime/traces/`

### 3. Explicit runtime controls
Compiler-aware runtime state should track:
- `runtime/active-sleeve.json`
- `runtime/active-stack.json`

### 4. Repo config expectations
Surfaced config signals include:
- compiler enabled = true
- compiler path = `./compiler`
- compiler mode = `local_repo_asset`

## Risks
- compiler v0.2/OpenClaw integration is referenced but not executed in the batch
- some setup guidance was CLI-version sensitive and corrected later
- compiler doctrine is operationally strong but still staged rather than complete
