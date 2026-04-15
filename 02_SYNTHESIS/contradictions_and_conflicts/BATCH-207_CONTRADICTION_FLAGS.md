# BATCH-207 — Contradiction / Ambiguity Flags

## Contradiction Watch
HIGH

## Main Flags
### 1. CLI Durability
Terminal interaction remained unstable and multiple fixes were proposed without one final solution.

### 2. Browser UI Pending
The browser plan is structurally strong but still depended on later bundle generation/integration.

### 3. Agents.v1.json State
This file remained provisional, stubbed, or warning-producing rather than a settled metadata model.

### 4. Patch/Bundle Quality
Some generated tarballs or patches had flaws in pathing, encoding, or package metadata.

### 5. Runtime Contract Normalization
`PoeRuntimeAgent.handle(...)` behavior was assumed in planning but not fully normalized across every path.

### 6. Surface Priority Tension
It remained open whether natural-language terminal interaction should keep priority or whether browser UI should fully take over.

## Intake Conclusion
Use this batch for:
- runtime stabilization docs
- loader and route consolidation
- Poe browser migration planning
- stack/sleeve inspection features

Do not use it alone to settle:
- final CLI architecture
- final browser contract
- final agent metadata model
- final patched file quality
