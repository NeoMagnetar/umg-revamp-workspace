# BATCH-027 — SLEEVE EXTRACT

## Sleeve Identity Signal
- Draft sleeve ID: `SLV.OPENCLAW.ULTIMA_OUTLANDS_RAZOR.v0.DRAFT`
- Operational framing: Outlands Razor operations sleeve
- Scope emphasis: move the user from fresh install to working automation profile
- Negative framing: not a broad Ultima Online helper

## Sleeve Responsibilities
- route by operational intent
- support setup and client sanity
- support UI operations and standard assistant behavior
- support script install and authoring
- account for Outlands-specific scripting deltas
- troubleshoot runtime failures
- expose reusable workflow families
- maintain compliance awareness around shard restrictions

## Proposed Stack Surface
- `NSTK.OUTLANDS.CLIENT_SETUP.v1`
- `NSTK.RAZOR.UI_OPERATIONS.v1`
- `NSTK.RAZOR.SCRIPT_INSTALL.v1`
- `NSTK.RAZOR.SCRIPT_AUTHORING.v1`
- `NSTK.OUTLANDS.SCRIPT_EXTENSIONS.v1`
- `NSTK.TROUBLESHOOTING.RUNTIME.v1`
- `NSTK.PLAYSTYLE.WORKFLOW_LIBRARY.v1`
- `NSTK.OUTLANDS.COMPLIANCE_AWARENESS.v1`

## Sleeve-Level Takeaway
This batch is strong evidence that a sleeve should set operational identity, scope, guardrails, and routing posture, while the actual domain cognition is distributed across modular stacks.

## Sleeve Cautions
- Identity is explicitly draft-state.
- Stack layout is recommended architecture, not a finalized deployed sleeve.
